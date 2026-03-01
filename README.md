# ai-api-scripts


CLI Scripts for openai API, using fish, macOS, curl, jq.

# aiquery
- Constraint file can be add to prompt. 
- creates log entry
- outputs response to Mac clipboard
- tracks token usage

## Files:
- Output files ~/Documents/openai
- Constraint files ~/Documents/openai/constraints
- Log ~/Documents/openai/_logs
 
## Arguments:
- -q query: The question to be to sent the API. If not given the query comes from stlin. 
- -f filename: Sets filename, if not suppiled the default filename is first 60 characters of prompt, appends the date and time to beginning of file.
- -m model: Model of API, this determines the cost and 
- -t temp: Determines the amount of effort
- -c constraint: file containing constraints and directives sent to API
 
## Usage:
``` fish
aiquery -p "Robot vacuum market in China in 2026" \
        -f "China Robot Vacuum Market 2026" \
        -c research.md
```

# aiprompt:
- outputs to stdout by default
- creates log entry
- outputs response to Mac clipboard
- tracks token usage
  
## Files:
- Output ~/Documents/openai must use write flag
- Logs ~/Documents/openai/_logs
 
## Arguments:
- -q prompt: The question to be to sent the API. If not given the question comes from stlin. 
- -f filename: sets filename, the default filename is first 60 characters of prompt, appends the date and time to beginning of file.
- -m model: Model of API, this determines the cost and 
- -t temp: Determines the amount of effort
- write : must include flag to create output file in openai dir
 
## Usage:
``` fish
aiprompt -p "Explain multipolarity." -f "Multipolarity Analysis" --write
```

