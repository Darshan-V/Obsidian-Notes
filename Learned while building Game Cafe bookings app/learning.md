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
