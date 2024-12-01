# ✨ **GitOps Sample** ✨

_A description of my project that blends travel, automation, and whimsy._

---

## Table of Contents
1. [🖼️ Images](#-images)
   - [Kazakhstan](#kazakhstan)
   - [Malaysia](#malaysia)
2. [🌏 Travel Parameters](#-travel-parameters)
3. [Simple Link](#simple-link)

## 🖼️ Images:

### Kazakhstan:

<p align="center">
  <img src="images/kazakh.jpg" alt="kazakh" width="200"/>
  <img src="images/kazakh-1.jpg" alt="kazakh" width="200"/>
  <img src="images/kazakh-2.jpg" alt="kazakh" width="200"/>
</p>


---

### Malaysia:  

<p align="center">
  <img src="https://as1.ftcdn.net/v2/jpg/01/83/57/50/1000_F_183575057_Ds4e51TuR08IasMWY9cgJOhJkT0quSzx.jpg" alt="Malay" width="200"/>
  <img src="images/malay.jpg" alt="Malay" width="200"/>
  <img src="images/malay-1.jpg" alt="Malay" width="200"/>
  <img src="images/malay-2.jpg" alt="Malay" width="200"/>
</p>

---

## 🌏 **Travel Parameters**

Here is the data for heading abroad:

| Parameter          | Value                  |
|--------------------|------------------------|
| **Name**           | `Rob's Whiter Half`   |
| **Class**          | `Class 5.5`           |
| **Desired Income** | `NaN`                 |
| **Desired Region** | `Asia`                |
| **Planned Countries** | `Thailand, Malaysia, Kazakhstan, Japan`|
| **Favorite Features** | `Mostly agree with Rob....Boob guy all day and horrible teeth are a no-go,needs to be skinny too`|

---

## Code Formatting with Bash Commands

### 🌐 REST API Interaction with `curl`

Examples of interacting with a REST API using `curl` and parsing data with`jq`.

---

### 🛠️ Setup
Before starting, ensure you have:
- **`curl`**: Command-line tool for making HTTP (and other) requests.
- **`jq`**: JSON processor for formatting and parsing JSON responses.

---

### 📝 REST Method Summary

| Method     | Purpose              | Example Command                                 |
|------------|----------------------|-----------------------------------------------|
| **GET**    | Retrieve data        | `curl -X GET https://api.example.com/tasks`    |
| **POST**   | Create new data      | `curl -X POST https://api.example.com/tasks`   |
| **PUT**    | Update existing data | `curl -X PUT https://api.example.com/tasks/{id}` |
| **DELETE** | Remove data          | `curl -X DELETE https://api.example.com/tasks/{id}` |

#### **POST** - Create Data with JSON data and JQ
```bash
curl -s -X POST https://api.example.com/tasks \
  -H "Content-Type: application/json" \
  -d '{"title": "Buy groceries", "due_date": "2024-12-01"}' | jq
```

- `-X POST`: Specifies the HTTP POST method to create new data.
- `-H "Content-Type: application/json"`: Sets the request's content type to JSON.
- `-d '{"key": "value"}'`: Sends the data in JSON format to create a new resource.
- `| jq`: Passes the response through `jq` to format and pretty-print the JSON response.



#### **PUT** - Create Data with JSON data and JQ
```bash
curl -s -X PUT https://api.example.com/tasks/123 \
  -H "Content-Type: application/json" \
  -d '{"title": "Buy groceries and snacks", "due_date": "2024-12-02"}' | jq
```

- `-X PUT`: Specifies the HTTP PUT method to update existing data.
- `https://api.example.com/tasks/123`: Targets the task with ID `123` to update its information.
- `-H "Content-Type: application/json"`: Sets the content type of the request to JSON.
- `-d '{"key": "value"}'`: Sends the new data as JSON to update the resource.
- `| jq`: Passes the JSON response through `jq` to format and print it in a readable form.

---

## Project Structure

- ./
    - .gitignore
    - README.md
    - images/
        - kazakh-1.jpg
        - kazakh-2.jpg
        - kazakh.jpg
        - malay-1.jpg
        - malay-2.jpg
        - malay.jpg
        - thai.jpg
    - scripts/
        - setup.sh
        - tree.py

### How to make your directory tree

[Directory Structure Script](./scripts/tree.py)