1. Set Up Your Project

    Initialize a new project:
    Create a new folder and run:

npm init -y

Install Tailwind CSS as a dev dependency:

    npm install -D tailwindcss

2. Configure Tailwind

    Generate a Tailwind config file:

    npx tailwindcss init

    This creates a tailwind.config.js file where you can customize Tailwind if needed.

3. Create Your Input CSS File

    Make a file named input.css and add the Tailwind directives:

    @tailwind base;
    @tailwind components;
    @tailwind utilities;

4. Build the CSS

    Compile your CSS file using the Tailwind CLI:
    Run the following command to generate your CSS file (e.g., output.css):

    npx tailwindcss -i ./input.css -o ./output.css --watch

    The --watch flag will rebuild your CSS automatically when you make changes. For a one-time build, you can omit it.

5. Link the Compiled CSS in Your HTML

    Create a basic HTML file and include the generated CSS:

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tailwind Local Example</title>
  <link rel="stylesheet" href="output.css">
</head>
<body class="bg-gray-100 p-8">
  <h1 class="text-3xl font-bold underline">Hello, Tailwind!</h1>
  <p>This is a simple HTML file using Tailwind loaded locally.</p>
</body>
</html>

