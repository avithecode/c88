Automobile Blockchain System
=====================


In this activity, you will create an app which will validate a block and represent invalid blocks by different colors in an automobile system.


* Open the file blockchain.py.
* Find the previous block from the block chain by reducing the index position by 1.


    `previousBlock = self.chain[currentBlock.index - 1]`
* Check whether the current block hash, greater than the previous block index, is equal or not and return false accordingly. .


` if(currentBlock.index != previousBlock.index + 1):
            return False
* Calculate hash for previousBlock and store it in previousBlockhash.


    `previousBlockHash = previousBlock.calculateHash()`
* Set the previous block hash to a wrong value when the current block index becomes 2.


`if(currentBlock.index == 2):
            previousBlockHash = previousBlock.calculateHash(time())`


* Check whether the previous block hash and current block hash is equal or not and return true or false accordingly. 
` if(previousBlockHash != currentBlock.previousHash):
            return False
        return True`


* Open the file app.py.
* Validate the new block using the chain.validateBlock()method and store it in a variable.


`isValid = chain.validateBlock(newBlock)`
* Set the value of the isValid method as isValid.


`newBlock.isValid = isValid`


* Open the file index.html.
* Change the background color of the invalid block to red.


`<div class="accordion-item" {%if block.isValid==false %} style="background-color: red;" {% endif %}>`


* Save and run the code to check the output.