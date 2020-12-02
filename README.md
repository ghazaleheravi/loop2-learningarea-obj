# loop2-learningarea-obj
<!doctype html>
<html lang="en-us" dir="ltr">
    <head>
        <meta charset="utf-8">
        <title>loop2</title>
    </head>

    <body>
        <div>
            <label for="input">Enter name: </label>
            <input id="input" type="text">
            <button>search</button>
        </div>
        <p></p>
       

        <script>
            let name = document.querySelector('#input');
            let button = document.querySelector('button');
            let para = document.querySelector('p');

            button.addEventListener('click',search);

            function search(){
                let Name = name.value.toLowerCase();
               
                let phonebook = [{name: 'mary', number:123456},{name: 'ghazaleh', number: 234567}];
                let i = 0;
               
                while(i<phonebook.length){
                    let nameprop =  phonebook[i]['name'];
                    let numberval = phonebook[i]['number'];
                    i++;
                    if(nameprop.toLowerCase()=== Name){
                       para.textContent = `${nameprop}'s number is ${numberval}`;
                       break;
                    }else{
                       para.textContent = 'contact not found.'; 
                    } 
           
                    }
                
                name.focus();
                name.value = '';
            }


            

        </script>
    </body>
</html>
