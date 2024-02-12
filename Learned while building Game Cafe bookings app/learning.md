snack bar
```<div className="flex flex-row w-full">

<span className="uppercase text-xs font-thin text-white">

Make A Booking &gt; &nbsp;

</span>

  

<span

className={`uppercase ${

modalNav === "seat" ? "underline" : ""

} underline-offset-4

font-thin text-xs text-white `}

>

select seats {modalNav === "hour" ? ">" : ""}

{modalNav === "seat" && <>&nbsp;</>}

</span>

{modalNav === "hour" && (

<span

className={`uppercase ${

modalNav === "hour" ? "underline" : ""

} underline-offset-4

font-thin text-xs text-white `}

>

choose hours

</span>

)}

</div>
```

### dist folder
The `dist` folder in a React project typically stands for "distribution" and is short for the distribution folder. It's a directory that contains the files and assets optimised for production deployment.

When you build a React application for production using a tool like Create React App or another build system, the optimised and minified versions of your JavaScript, CSS, and other assets are generated. These optimised files are then placed in the `dist` folder.

The contents of the `dist` folder are the ones you would deploy to a web server or a hosting service for your production application. The goal is to have a streamlined and efficient version of your application that reduces file sizes, combines files where possible, and applies various optimisations for faster loading times.

It's worth noting that the actual name of this folder might vary depending on the build configuration or the tools you're using. For example, in Create React App, the default output folder is `build`. Other build tools or custom configurations might use `dist` or another name.

In summary, the `dist` folder contains the production-ready version of your React application, optimised for performance and ready to be deployed.