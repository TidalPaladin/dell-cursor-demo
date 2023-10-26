# Dell Cursor Demo

Demo of [Cursor](https://cursor.sh/), a VSCode fork with GPT-4 integration.

## Commands

Create `dell_cursor_demo/process.py`.

```
Write a python script that accepts and input dir and and output dir and does the following:
* Finds all JSON files in the input dir.
* Reads each JSON file
* Extract the field "name" which contains full names in style "First M Last" or "First Last"
* Pop the "name" field and make sure that the name does not appear in any other field in the JSON
* Save the updated JSON to the output dir using the extracted "name". The output file should be saved in a subdir as style LAST^FIRST^M/report.json or LAST^FIRST/report.json, where ^ is a separator and the name components are all capitalized.

Use a tqdm bar to indicate progress. Raise NotADirectoryError if any of the given dirs do not exist. Raise a FileNotFoundError if you find no JSONs in the input dir.
```

Create `tests/test_process.py`.

```
Write unit tests for @process_jsons
```

In `dell_cursor_demo/process.py`:

```
Write a CLI interface for process_jsons
```

Run the CLI tool on the `data` directory.

```bash
pdm run python dell_cursor_demo/process.py data/ output/
```

Chat

```
What does process_jsons do?
```

```
Give me some examples of how it will transform the "name" key into a directory name
```

CLI

```
Find all .json files in the output dir and print only their parent directory name
```