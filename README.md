# Simple-Crud-App
CRUD app code and .md file explaining code with pictures
This is a basic CRUD (Create, Read, Update, Delete) web application built with Flask (or Django/FastAPI).

## 📸 Screenshot

![CRUD UI](static/images/crud-ui.png)

---

## 🔧 Features

- Create new records
- Read/display existing records
- Update records
- Delete records

---

## 💡 How it Works

### 1. Create

```python
@app.route('/create', methods=['POST'])
def create():
    name = request.form['name']
    user = User(name=name)
    db.session.add(user)
    db.session.commit()
    return redirect('/')
