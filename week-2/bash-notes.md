# Week 2 - bandit labs

## **Level 0**

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
cat readme
```

## **Level 1**
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
cat ./-
```

## **Level 2**
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
cat spaces\ in\ this\ filename
```

## **Level 3**
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
cd inhere
ls -la
cat .hidden
```

## **Level 4**
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
cd inhere
for i in $(ls); do file ./$i; done
# Found "ASCII text" (-file07)
cat ./-file07
```

## **Level 5**
```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
cd inhere
(find -type f | xargs ls -l 2>/dev/null) | grep 1033
# Found file "./maybehere07/.file2"
cat ./maybehere07/.file2
```

## **Level 6**
```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
find / -type f -user bandit7 -group bandit6 2>/dev/null
# Found "/var/lib/dpkg/info/bandit7.password"
cat /var/lib/dpkg/info/bandit7.password
```

## **Level 7**
```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
cat data.txt | grep millionth
```

## **Level 8**
```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
cat data.txt | sort | uniq -u
```

## **Level 9**
```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
strings data.txt | grep ==
```

## **Level 10**
```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
cat data.txt | base64 -d
```