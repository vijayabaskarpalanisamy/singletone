# singletone
public class SingleObject
{
//original object is created for the SingleObject class
static SingleObject obj=new SingleObject(); //Early Initialization

// Object for SingleObject class returned in this method
public static SingleObject getInstance()
{
return obj;
}
public void show()
{
System.out.println("Method1");
}
public static void main(String[] args)
{
// Object create by refer the other Object
SingleObject s3=SingleObject.getInstance();
SingleObject s4=SingleObject.getInstance();
s3.show();
//hashcode for both object are same && revise the shallow copy concept
System.out.println(s3);
System.out.println(s4);

}


}



******************************Lazy Initialization********************************
    
public class SingleObject
{
//original object is created for the SingleObject class
static SingleObject obj=null; //lazy Initialization

// Object for SingleObject class returned in this method
public static SingleObject getInstance()
{
if(obj==null)
{
obj=new SingleObject();
}
return obj;
}
public void show()
{
System.out.println("Method1");
}
public static void main(String[] args)
{
// Object create by refer the other Object
SingleObject s3=SingleObject.getInstance();
SingleObject s4=SingleObject.getInstance();
s3.show();
//hashcode for both object are same && revise the shallow copy concept(one object is reference to another)
System.out.println(s3);
System.out.println(s4);

}
}
