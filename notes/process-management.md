# Task 4: Process Management

## Objective
The goal of this task was to learn how to manage processes in Linux by running a background process, identifying it, and then terminating it using its Process ID (PID).

---

## Steps I Took

I started by running a long-running process in the background using:

sleep 100 &

This command runs the `sleep` process for 100 seconds in the background.

The terminal returned:

[1] 12508

This means:
- `[1]` is the job number
- `12508` is the Process ID (PID)

---

Next, I checked the running jobs using:

jobs

This showed that the `sleep 100` process was still running in the background.

---

To find more details about the process, I used:

ps aux | grep sleep

This displayed the running `sleep` process along with its PID, confirming it was active.

---

## Mistake I Made

I initially tried to stop the process using:

kill <PID>

This caused an error:

zsh: parse error near `\n'

The mistake was that `<PID>` is not an actual command. It is just a placeholder used in instructions and should be replaced with the real Process ID.

---

## How I Fixed It

After understanding the mistake, I replaced `<PID>` with the actual process ID shown earlier (12508) and ran:

kill 12508

This successfully terminated the background `sleep` process.

Alternatively, I also learned I could use:

kill %1

to stop the process using the job number instead of the PID.

---

## Outcome

The background process was successfully stopped, completing the task requirements.

---

## Commands Learned

### sleep 100 &
Runs a process in the background for 100 seconds.

### jobs
Shows all currently running background jobs.

### ps aux | grep sleep
Finds running processes related to "sleep".

### kill <PID>
Terminates a process using its Process ID.

### kill %1
Terminates a process using its job number.
