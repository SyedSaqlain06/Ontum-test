function pow(n,m,d){ var temp=n; for(var i=1;i<m;i++){
               temp=temp*n;
               temp=parseInt(temp.toString().slice(-d,))
             }
           return temp
           }        
        var out=0;
        var t=0;
        for(var j=1;j<=1000;j++){
            t=pow(j,j,10);
            <!--t=Math.pow(j,j)--> out+=t; <!--console.log(t);--> }
out=parseInt(out.toString().slice(-10,))
