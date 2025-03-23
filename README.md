Showcase web app for CI/CD training.

Each student adds a card with their info and project.

## Run locally
```bash
pip install fastapi uvicorn jinja2
cd app
uvicorn main:app --reload
```

## Add your card
Edit `students.json` and add yourself:
```json
{
  "name": "Your Name",
  "github": "https://github.com/yourname",
  "project": "My Cool Script",
  "avatar": "https://i.pravatar.cc/150?u=yourname"
}
```

Push your change and once CI/CD passes — it will be live!
