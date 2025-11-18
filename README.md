**1. Interface vs Type**

**a.** Interface শুধুমাত্র object-এর shape define করতে বেশি ব্যবহৃত হয়।
**b.** Type দিয়ে union, primitive alias define করা যায়।
**c.** Interface extend করা হয় extends কীওয়ার্ড ব্যবহার করে। 
**d.** Type extend করা হয় & (intersection ) ব্যবহার করে।
**e.** Union, Intersection, Conditional Type—এগুলো Interface দিয়ে করা যায় না।

**Example of Interface:**
```ts
    interface Animal {
      name: string;
    }

    interface Dog extends Animal {
      breed: string;
    }
```

**Example of Type:** 
```ts
type Animal = {
  name: string;
};

type Dog = Animal & {
  breed: string;
};
```

**2.Use of the keyof keyword in TypeScript**
TypeScript-এ keyof keyword ব্যবহার করা হয় কোনো object type-এর সবগুলো key-এর নামকে একটি union type হিসেবে পাওয়ার জন্য। Object-এর key-গুলো ভুল লেখা থেকে বাঁচায়।

**Example of keyof :**
```ts
type User = {
name: string;
age: number;
email: string;
};
type UserKeys = keyof User; 
// UserKeys = "name" | "age" | "email"
```






