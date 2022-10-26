#Longest Word

Have the function LongestWord(sen) take the sen parameter being passed and return the longest word in the string. If there are two or more words that are the same length, return the first word from the string with that length. Ignore punctuation and assume sen will not be empty. Words may also contain numbers, for example "Hello world123 567"

####Answer:

````
function LongestWord(sen) {
  let longestWord = ""
  let array = sen.trim().replace(/[^a-zA-Z0-9 ]/g, '').split(" ")
  array.forEach(word => {
    if (word.length > longestWord.length) {
      longestWord = word
    }
  })
  return longestWord
}