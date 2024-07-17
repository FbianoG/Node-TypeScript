# Node + TypeScript
### How create a application with Node.js + TypeScript

1. Init the project:
```bash
npm init
```
  
3. Install the dependences TypeScript:
```bash
npm install typescript ts-node @types/node @types/express nodemon -D
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

