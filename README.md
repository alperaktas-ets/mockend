<!-- @format -->

## Config

Create a `.mockend.json` file with the following basic config:

==github.com/alperaktas-ets/mockend/.mockend.json==

```json
{
	"User": {
		"title": { "string": {} }
	}
}
```

## Try It

Try the new mock server:

```bash
# 1. List your fake users with a GET request
curl https://mockend.com/org/repo/users

# 2. Fake a creation with a POST
# (don't worry changes aren't persisted)
curl https://mockend.com/org/repo/users \
  -X POST \
  -H "Content-Type: application/json" \
  --data '{"name": "alice"}'
```

- Access your GraphQL endpoint: https://mockend.com/org/repo/graphql

## Random Generator Config

==github.com/alperaktas-ets/mockend/.mockend.json==

```json
{
	"User": {
		"name": {
			"string": {}
		},
		"avatarUrl": {
			"regexp": "https://i\\.pravatar\\.cc/150\\?u=[0-9]{5}"
		},
		"statusMessage": {
			"string": ["working from home", "watching Netflix"]
		},
		"email": {
			"regexp": "#[a-z]{5,10}@[a-z]{5}\\.[a-z]{2,3}"
		},
		"color": {
			"regexp": "#[0-9A-F]{6}"
		},
		"age": {
			"int": {
				"min": 21,
				"max": 100
			}
		},
		"isPublic": {
			"boolean": {}
		}
	}
}
```
