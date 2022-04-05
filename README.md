# JavaScript--Turn-Strings-into-Title-Case

const convertTitleCase = function (title) {
  const capitalize = (str) => str[0].toUpperCase() + str.slice(1);
  const exceptions = [  "a", "an","am", "are", "is","and", "the","but", "or", "on", "in",
    "with" ];
  const titleCase = title
    .toLowerCase()
    .split(" ")
    .map((word) => (exceptions.includes(word) ? word : capitalize(word)))
    .join(" ");

  return capitalize(titleCase);
};
console.log(convertTitleCase("i am a title"));
console.log(convertTitleCase("i a Big fat long title"));
