## Main Directories
```shell
/                          # Root of entire system
├── home/                  # User home directories
│   └── username/          # Your personal space
├── usr/                   # User programs and libraries
│   ├── bin/              # User programs (like cargo, rustc)
│   └── local/            # Locally installed software
└── tmp/                  # Temporary files

`~`: Your home directory
`.`: Current directory
`..`: Parent directory
`/`: Root directory

pwd: print working directory
cd directory_name: change directory to directory_name

```
## ls
```shell
ls...: #lists files in the current working directory

ls -l: #longer format of ls

ls -a: #shows all files, including hidden files (can be combined as -la or -al)

ls -lh: #like -l but more readable

ls -lt: #sorts longer format by date modified
```

## grep (Global Regular Expression Print)

```shell
grep: #grep [OPTIONS] regex_pattern file_name/directory
grep -i ...: #case-insensitive search
grep -r ...: #recursive search
grep -n ...: #show the line number of matches
grep -v ...: #similar to -n, instead inverted showing the number of non-matches
grep -c ...: #show the count of matching lines
```

## mkdir

```shell
mkdir new_directory: #creates a new directory

mkdir /path/to/new_folder: #created a new directory at a specific path

mkdir -p ...: #creates a nested directory
```

## touch
```shell
touch file_name: #creates an empty file
```

## echo
```shell
echo ...: #prints out a string (or variable if preceded by a $)

echo ... > file_name: #overwrites the file with the contents from the echo command

echo... >> file_name: #appends the file with the contents from the echo
```

## Reading a File

```shell
cat file_name: #displays the file
head file_name: #displays the file's first 10 lines
tail file_name: #displays the file's last 10 lines
less file_name: #allows the viewing of the file page by page (quittable with q)
nano file_name: #edit a file

cp source_text.txt destination.txt #copies the contents from the source text to the destination text
mv old_name.txt new_name.txt #renames the file from its old name to a new one
rm file_name.txt #deletes the file and its contents
rm -r directory_name #deletes the directory and its contents
rm -rf directory_name #like rm -rf, but bypassing the additional confirmation of deletion

```

## Running a Rust File
```shell
rustc main.rs
./main
```