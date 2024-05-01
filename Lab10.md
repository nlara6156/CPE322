## Lab 10

```
PS C:\Users\nadia\iot\lesson10> cat hash_value.py
"""
https://docs.python.org/3/using/cmdline.html#envvar-PYTHONHASHSEED
If PYTHONHASHSEED is not set or set to random, a random value is used to to seed the hashes of str and bytes objects.
If PYTHONHASHSEED is set to an integer value, it is used as a fixed seed for generating the hash() of the types covered by the hash randomization.
Its purpose is to allow repeatable hashing, such as for selftests for the interpreter itself, or to allow a cluster of python processes to share hash values.
The integer must be a decimal number in the range [0,4294967295]. Specifying the value 0 will disable hash randomization.

https://www.programiz.com/python-programming/methods/built-in/hash
hash(object) returns the hash value of the object (if it has one). Hash values are integers.
They are used to quickly compare dictionary keys during a dictionary lookup.
Numeric values that compare equal have the same hash value even if they are of different types, as is the case for 1 and 1.0.
For objects with custom __hash__() methods, note that hash() truncates the return value based on the bit width of the host machine.
"""

# hash for integer unchanged
print('The hash for 1 is:', hash(1))

# hash for decimal
print('The hash for 1.0 is:',hash(1.0))
print('The hash for 3.14 is:',hash(3.14))

# hash for string
print('The hash for Python is:', hash('Python'))

# hash for a tuple of vowels
vowels = ('a', 'e', 'i', 'o', 'u')
print('The hash for a tuple of vowels is:', hash(vowels))

# hash for a custom object
class Person:
    def __init__(self, age, name):
        self.age = age
        self.name = name
    def __eq__(self, other):
        return self.age == other.age and self.name == other.name
    def __hash__(self):
        return hash((self.age, self.name))
person = Person(23, 'Adam')
print('The hash for an object of person is:', hash(person))
```

### Run #1 of Hash Value

```
PS C:\Users\nadia\iot\lesson10> python3 hash_value.py
The hash for 1 is: 1
The hash for 1.0 is: 1
The hash for 3.14 is: 322818021289917443
The hash for Python is: -8618236071167298098
The hash for a tuple of vowels is: 9185075461943906823
The hash for an object of person is: -4111237402702381223
```

### Run #2 of Hash Value

```
PS C:\Users\nadia\iot\lesson10> python3 hash_value.py
The hash for 1 is: 1
The hash for 1.0 is: 1
The hash for 3.14 is: 322818021289917443
The hash for Python is: 7837300043454952309
The hash for a tuple of vowels is: -8255807982862756380
The hash for an object of person is: 3716378598450869949
```

### Tiniest Blockchain (Run of snakecoin.py)

```
PS C:\Users\nadia\iot\lesson10> python3 snakecoin.py
Block #1 has been added to the blockchain!
Hash: e38522352fb6f95bd36e2eaa0b1dd393514126846da7bb84d78bebf60cccfa26

Block #2 has been added to the blockchain!
Hash: e9ece3239510ebde9e299ae8c887e398e61dfccc74fd599c402effdc24bed5a2

Block #3 has been added to the blockchain!
Hash: 8515043eee8cf43a758a86918f4c2c52ca4a9e87b4a591d1ebe8a29f8fc08ead

Block #4 has been added to the blockchain!
Hash: 2cd16937d1031b042b5e4d98f6f0ed3e1c6cfd0574f06ae47c2c1f24b4549233

Block #5 has been added to the blockchain!
Hash: 898ca588ecc3eebc036ecd00585e028e8b72f1917cade64206213fb1bcb5f957

Block #6 has been added to the blockchain!
Hash: 6e2e2f760f55c7c4268c597862fcf093f97add013d13714443eb9c3e490fd22d

Block #7 has been added to the blockchain!
Hash: 1084dc3be1143890d8c227169183abfd4405dda36ef77e5f9179a2860516b093

Block #8 has been added to the blockchain!
Hash: 427ee13d576d4c42a9ae47dc6673bb5ba8821c182850dd040b68e441175b4f8f

Block #9 has been added to the blockchain!
Hash: 9f3194fabed759d0a9923e99c4e49f88e6ced39f5283df295c92c2412089372f

Block #10 has been added to the blockchain!
Hash: 6ea343e396be87bc641a97e87027ff513f59d6b2ed147e8966e658640b8c9b3c

Block #11 has been added to the blockchain!
Hash: d8bdae2583729c84cde406f3f1e844330ad0e026f746af5d7c63e10162d408c4

Block #12 has been added to the blockchain!
Hash: 581328b5f02f2efca371d42f57bf11c2dcade193c99c6f3bd30c45d4a516e918

Block #13 has been added to the blockchain!
Hash: cb24c2147a45e01d84b1a01043ed32d45ab964a9a5717fa133331a8b5cc11ebc

Block #14 has been added to the blockchain!
Hash: 49084effa25f31a85ae73f530aab96e75b78b492995aaa8c7ce6d4ae36c34414

Block #15 has been added to the blockchain!
Hash: 2cae77e4ee5860990bc889086952f0cfcdaed7cf46ef926f2bdf46ec237e15b6

Block #16 has been added to the blockchain!
Hash: 232289b02c561e42ab3ccf4ca9cd8d6e28b7b1751625a2520313040b50124739

Block #17 has been added to the blockchain!
Hash: 03d5421764133b1bf72a0dbc01d11313d771647a8f4da98fe5d1ed6b911bfdea

Block #18 has been added to the blockchain!
Hash: 5a2a85e928528e0b99fd5dafca42d98dd9624f8b3f2452d2400fe6ad6e577cc8

Block #19 has been added to the blockchain!
Hash: 82c6a90d55cf63ac023264c3bdca0f93dc22f02add9af37e724b0f0c4fc53b37

Block #20 has been added to the blockchain!
Hash: 2000d88e1207889562d273d28f5941f1a6000de9e67205b60647b21f2c507253
```

### Make Blockchain BIgger (Snakecoin-server-full-code.py)

```
PS C:\Users\nadia\iot\lesson10> cat snakecoin-server-full-code.py
# Gerald Nash, "Letâ€™s Make the Tiniest Blockchain Bigger Part 2: With More Lines of Python"
# Referred to https://www.pythonanywhere.com/forums/topic/12382/ that fixed sha.update() TypeError: Unicode-objects must be encoded before hashing
# Running on http://127.0.0.1:5000/mine (Reload the page to mine and press CTRL+C to quit)
from flask import Flask
from flask import request
import json
import requests
import hashlib as hasher
import datetime as date
from flask import send_from_directory
import os
node = Flask(__name__)

# Define what a Snakecoin block is
class Block:
  def __init__(self, index, timestamp, data, previous_hash):
    self.index = index
    self.timestamp = timestamp
    self.data = data
    self.previous_hash = previous_hash
    self.hash = self.hash_block()

  def hash_block(self):
    sha = hasher.sha256()
#    sha.update(str(self.index) + str(self.timestamp) + str(self.data) + str(self.previous_hash))
    sha.update((str(self.index) + str(self.timestamp) + str(self.data) + str(self.previous_hash)).encode("utf-8"))
    return sha.hexdigest()

# Generate genesis block
def create_genesis_block():
  # Manually construct a block with
  # index zero and arbitrary previous hash
  return Block(0, date.datetime.now(), {
    "proof-of-work": 9,
    "transactions": None
  }, "0")

# A completely random address of the owner of this node
miner_address = "q3nf394hjg-random-miner-address-34nf3i4nflkn3oi"
# This node's blockchain copy
blockchain = []
blockchain.append(create_genesis_block())
# Store the transactions that
# this node has in a list
this_nodes_transactions = []
# Store the url data of every
# other node in the network
# so that we can communicate
# with them
peer_nodes = []
# A variable to deciding if we're mining or not
mining = True

@node.route("/")
def hello():
    return "SnakeCoin Server"

@node.route('/favicon.ico')
def favicon():
    return send_from_directory(os.path.join(node.root_path, 'static'),
                               'favicon.ico',
                               mimetype='image/vnd.microsoft.icon')

@node.route('/txion', methods=['POST'])
def transaction():
  # On each new POST request,
  # we extract the transaction data
  new_txion = request.get_json()
  # Then we add the transaction to our list
  this_nodes_transactions.append(new_txion)
  # Because the transaction was successfully
  # submitted, we log it to our console
  print("New transaction")
  print(("FROM: {}".format(new_txion['from'].encode('ascii','replace'))))
  print(("TO: {}".format(new_txion['to'].encode('ascii','replace'))))
  print(("AMOUNT: {}\n".format(new_txion['amount'])))
  # Then we let the client know it worked out
  return "Transaction submission successful\n"

@node.route('/blocks', methods=['GET'])
def get_blocks():
  chain_to_send = blockchain
  # Convert our blocks into dictionaries
  # so we can send them as json objects later
  for i in range(len(chain_to_send)):
    block = chain_to_send[i]
    block_index = str(block.index)
    block_timestamp = str(block.timestamp)
    block_data = str(block.data)
    block_hash = block.hash
    chain_to_send[i] = {
      "index": block_index,
      "timestamp": block_timestamp,
      "data": block_data,
      "hash": block_hash
    }
  chain_to_send = json.dumps(chain_to_send)
  return chain_to_send

def find_new_chains():
  # Get the blockchains of every
  # other node
  other_chains = []
  for node_url in peer_nodes:
    # Get their chains using a GET request
    block = requests.get(node_url + "/blocks").content
    # Convert the JSON object to a Python dictionary
    block = json.loads(block)
    # Add it to our list
    other_chains.append(block)
  return other_chains

def consensus():
  # Get the blocks from other nodes
  other_chains = find_new_chains()
  # If our chain isn't longest,
  # then we store the longest chain
  longest_chain = blockchain
  for chain in other_chains:
    if len(longest_chain) < len(chain):
      longest_chain = chain
  # If the longest chain isn't ours,
  # then we stop mining and set
  # our chain to the longest one
  blockchain = longest_chain

def proof_of_work(last_proof):
  # Create a variable that we will use to find
  # our next proof of work
  incrementor = last_proof + 1
  # Keep incrementing the incrementor until
  # it's equal to a number divisible by 9
  # and the proof of work of the previous
  # block in the chain
  while not (incrementor % 9 == 0 and incrementor % last_proof == 0):
    incrementor += 1
  # Once that number is found,
  # we can return it as a proof
  # of our work
  return incrementor

@node.route('/mine', methods = ['GET'])
def mine():
  # Get the last proof of work
  last_block = blockchain[len(blockchain) - 1]
  last_proof = last_block.data['proof-of-work']
  # Find the proof of work for
  # the current block being mined
  # Note: The program will hang here until a new
  #       proof of work is found
  proof = proof_of_work(last_proof)
  # Once we find a valid proof of work,
  # we know we can mine a block so
  # we reward the miner by adding a transaction
  this_nodes_transactions.append(
    { "from": "network", "to": miner_address, "amount": 1 }
  )
  # Now we can gather the data needed
  # to create the new block
  new_block_data = {
    "proof-of-work": proof,
    "transactions": list(this_nodes_transactions)
  }
  new_block_index = last_block.index + 1
  new_block_timestamp = this_timestamp = date.datetime.now()
  last_block_hash = last_block.hash
  # Empty transaction list
  this_nodes_transactions[:] = []
  # Now create the
  # new block!
  mined_block = Block(
    new_block_index,
    new_block_timestamp,
    new_block_data,
    last_block_hash
  )
  blockchain.append(mined_block)
  # Let the client know we mined a block
  return json.dumps({
      "index": new_block_index,
      "timestamp": str(new_block_timestamp),
      "data": new_block_data,
      "hash": last_block_hash
  }) + "\n"

node.run()
```

### Blockchain App
