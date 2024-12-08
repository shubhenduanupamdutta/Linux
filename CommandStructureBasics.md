# Command Structure Basics

---

## Understanding the Prompt

---

**When you start the terminal, you will see some text on left side of the screen. This text is called the _prompt_.**

**The prompt is a signal that the terminal is ready to accept your command.**

**The prompt usually includes some information about the system, like the username, hostname, and the current directory. `username@hostname:current_directory:~$`**

**The prompt can be customized to show more or less information.**

---

### Some Commands

---

- `clear`: _Clears the terminal screen._
- `date`: _Displays the current date and time._
- `ncal`: _Displays the calendar for the current month, in vertical format._
- `cal`: _Displays the calendar for the current month, in horizontal format._
- `echo`: _Prints the text that follows it._

---

## Command Structure

---

**Most commands support multiple `options` that modify their behavior. We can decide which options to include, if any, when we execute a command.**

**Similarly, mandy commands accept arguments (the things that the command acts upon or uses).**

```bash
$ command -options arguments
```

### Arguments

_The terms **"argument"** and **"parameter"** are often used interchangeably, and they both refer to the values that are passed to a command._

_The `echo` command is extremely simple, it takes the arguments we provide to it and prints them to the terminal._

```bash
$ echo Hello, World!
Hello, World!
```

#### Let's take an example of `ncal` command

```bash
$ ncal 2024
```

_This command will display the calendar for the year 2024._

```bash
$ ncal july 2021
```

_This command will display the calendar for the month of July in the year 2021._

**Here `2024` and `july 2021` are the arguments. As you can see, the `ncal` command can accept different types of arguments, and different amounts of arguments.**

**But if we give year first and then month, it will throw an error.**

---

### Options

---

**Each command typically supports a host of options that we can choose to use when executing the command. These options modify the behavior of the command in predefined ways.**

**Options are usually preceded by a `-` or `--`. For example `-h` or `-3`**

```bash
$ command -options
```

- `ncal -h`, where `-h` is an option, disables the default highlighting of the current day.
- `ncal -j` where `-j` is option, displays the calender using julian days (days are numbered from Jan 1).
- `ncal -M` where `-M` is option, displays the calendar where week starts from Monday.
- `ncal -3` where `-3` is option, displays the calendar for the previous, current, and next month.

### Combining Options

**We can provide multiple options at once. `ncal -3 -h` will display the calendar for the previous, current, and next month, and will disable the highlighting of the current day.**

**Alternatively, we can combine the options into a single argument. `ncal -3h` will do the same thing.**

### Long Form Options

**Some options also support equivalent long format options that are usually full words and are prefixed with two dashes `--` instead of one.**

**For example, the `date -u` option is used to print the date in UTC time. The long form equivalent is `date --universal`.**

### Options with Parameters

**Some options require us to pass in an additional value. For example, ncal's `-A` option requires a number to be passed in, and is used to display a certain number of months after a specific date.**

_This command will display the calendar for the next 3 months._

```bash
$ ncal -A 3
```

**Again, we can combine options with parameters. `ncal -A3` will do the same thing as `ncal -A 3`.**

### Combining Options with Parameters

**We can also combine options with parameters. `ncal -hA3 july 2024` will display the calendar for the 3 months (July, August and September) of 2024 and will disable the highlighting of the current day.**
