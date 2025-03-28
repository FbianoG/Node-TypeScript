# Node + TypeScript
### How create a application with Node.js + TypeScript

1. Init the project:
```bash
npm init
```
2. Install dependences:
```bash
npm install express mongoose cors
```
  
4. Install the dependences TypeScript and dev-dependences:
```bash
npm install typescript ts-node @types/node @types/express nodemon dotenv -D
```
     
5. Create document tsconfig.json in root:
```json
{
  "compilerOptions": {
    "target": "es2016", 
    "module": "commonjs", 
    "esModuleInterop": true, 
    "forceConsistentCasingInFileNames": true, 
    "strict": true, 
    "skipLibCheck": true,
    "outDir": "./dist",
    "rootDir": "./src"
  }
}
```
6. Include scripts in package.json:
```json
 "scripts": {
    "build": "tsc",
    "start": "node dist/index.js",
    "dev": "nodemon src/index.ts"
  },
```

7. Organization the files:
    - ![image](https://github.com/user-attachments/assets/3b9c0284-3265-4ebb-9ded-5bf52f46fd56)

8. Create document vercel.json in root:
```json
{"version": 2,
  "builds": [{"src": "src/index.ts",
    "use": "@vercel/node"}],
  "routes": [{"src": "/(.*)",
    "dest": "src/index.ts"}]}
```
