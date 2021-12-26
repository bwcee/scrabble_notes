# Scrabble Project Notes/ Resources

## External Notes

1. [Scrabbling with Javascript](https://medium.com/@valeriemccarthy/scrabbling-with-javascript-8c2ea48b5af5)<br>
   blog post on experience of building scrabble

## Strategy

1. build out the entire game in front end first then think about linking the back end
2. so just empty html page with script.js src to render

## Building Notes

1. API calls to 3rd party dictionary to confirm word submissions
2. how to render board -> nested array? it's a 15x15 board<br>

```
//in Board.js
buildBoardGrid(row, col){
    let square = null
    let boardArray = []    for(var tempRow = 0; tempRow < row; tempRow++){
        boardArray.push([])    boardArray[tempRow].push(new Array(col))    for(var tempCol = 0; tempCol < col; tempCol++){
          square = new Square(tempRow, tempCol)
          boardArray[tempRow][tempCol] = square.render()
        }
    }
    return boardArray
 }//In Square.js
render(){
    return `<div id="${this.tempRow}_${this.tempCol}" class="square" ></div>`
  }
```

3. arrays to keep track of letters at diff locations?
4. how to do drag and drop? there are libraries avail to do this at this [website](https://www.cssscript.com/best-drag-drop-javascript-libraries/)
5. dictionary api [WordsAPI](https://www.wordsapi.com/)
6. there are 100 tiles in scrabble ea with a letter and value, see [here](https://wordfinder.yourdictionary.com/blog/scrabble-letter-values-list/)<br>

## Random Resources

1. Someone's working scrabble game on github [here](https://github.com/edlerd/scrabble/blob/master/game.js)
2. Nice sample of ui [here](https://github.com/amnond/jscrab)
