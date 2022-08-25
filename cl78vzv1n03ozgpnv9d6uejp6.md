## Set up Assembly language Environment in Ubuntu 20.04

Install git if you don't have

```
sudo apt install git
```
or confirmed by
```
git -version
```
Then copy this command and paste it in terminal.
```
cd ~ ; mkdir Test; cd Test; git clone https://github.com/zexhan17/assembly-lang-course.git
```
wait until clone done.
```
cd assembly-lang-course;
```
Install unzip command to unzip .zip folders in terminal or you can unzip by GUI.
```
sudo apt install unzip
```
unzip AssmSoft.zip folder.
```
unzip AssmSoft.zip
```
Note: if you unzip using GUI move all unzip file to assembly-lang-course

# Install DOSBOX
```
sudo apt install dosbox
```
After, installation run dosbox command to run it.
```
dosbox
```
Now, in dosbox paste this command.
```
mount c ~/Test/assembly-lang-course
```
then
```
c:
```
Assemble a file
```
nasm c01-01.asm -o c.com
```
Run assembled file
```
afd c.com
```

Type quit in running file terminal to come back dosbox shell  

If after changing files, they do not show up in dosbox, hit Ctrl+f4 inside the dosbox window to make changes
