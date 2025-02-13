 The `sed` command is a stream editor used to perform basic text transformations on an input stream (a file or input from a pipeline). Here are some common switches:

 Substitute (replace) text
sed 's/old-text/new-text/' inputfile

 Substitute text globally (replace all occurrences in each line)
sed 's/old-text/new-text/g' inputfile

 Substitute text only on a specific line
sed '3s/old-text/new-text/' inputfile

 Delete lines matching a pattern
sed '/pattern/d' inputfile

 Print only lines matching a pattern
sed -n '/pattern/p' inputfile

 Insert text before a line matching a pattern
sed '/pattern/i\new-line-of-text' inputfile

 Append text after a line matching a pattern
sed '/pattern/a\new-line-of-text' inputfile

 Replace text in a specific range of lines
sed '5,10s/old-text/new-text/' inputfile

 Use a different delimiter instead of '/'
sed 's|old-text|new-text|' inputfile