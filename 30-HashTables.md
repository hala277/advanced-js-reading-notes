# Hash Tables

## What is a Hashtable, exactly?

+ Hash: A hash is the result of an algorithm that converts an entering string into a value that can be used for security or another purpose. It is used to find the index of the array in the case of a hashtable.
+ Buckets: A bucket is the content of each index of the hashtable's array. Each index corresponds to a bucket. If a collision happens, an index could include multiple key/value pairs.
+ Collisions: When more than one key is hashed to the same place in the hashtable, a collision occurs.

## Why do we use Hashtable?
1. Hold unique values
2. Dictionary
3. Library

## What Do Hashtables Mean?
Hashtables are a type of data structure that uses key-value pairs to store data. This means that each Node and Bucket has a key as well as a value.

The primary concept behind a hashtable is the ability to rapidly retrieve the information by storing the key in the data structure. This is accomplished through the use of a hash. A hash is the ability to encode a key that will eventually map to a specific spot in the data structure that we can look at to retrieve the item directly.

![Example on Hashtables](https://camo.githubusercontent.com/9ad322f07bd2a15c9ec9eca7bf8ab0ec2abcd05726ed9ddaffedf4ff2d9ac904/68747470733a2f2f75706c6f61642e77696b696d656469612e6f72672f77696b6970656469612f636f6d6d6f6e732f372f37642f486173685f7461626c655f335f315f315f305f315f305f305f53502e737667)

## Structure

### Hashing :
A hash code basically converts a key into an integer. The fact that hash codes are deterministic is crucial: their output is determined solely by their input. Randomness should never be used in hash codes. The hash code generated by the same key should always be the same.

### Creating a Hash

Traditionally, a hashtable is built from an array. Size 1024 can be used. This is crucial for index positioning. Make some form of logic to convert that "key" into a numeric number value after you've constructed your array of the suitable size. Here's something to consider:

+ Add or multiply all the ASCII values together.
+ Multiply it by a prime number such as 599.
+ Use modulo to get the remainder of the result, when divided by the total size of the array.
+ Insert into the array at that index.

#### Example:


```js

Key = "Cat"
Value = "Josie"

67 + 97 + 116 = 280

280 * 599 = 69648

69648 % 1024 = 16

Key gets placed in index of 16. 
```

Our key Cat now corresponds to index 16 in the array. We may rapidly look through this index and discover "Josie," our value.

### Collisions

When more than one key hashes to the same index in an array, a collision occurs. A "perfect hash" will never have any collisions, as previously stated. To put this in context, the worst conceivable hash is one that hashes every single key to the same exact array index. The more keys hashed to a specific index, the more key/value pair combinations you can have.

What would happen if two distinct keys resolved to the same array index? This is referred to as a collision. Two keys resolving to the same index must be handled by the hash map.

If two keys ever resolve to the same index, then two calls to will be required. Different keys would overwrite each other in Add(key, val).

![Hash collision resolved by separate chaining.](https://camo.githubusercontent.com/b5773cab5b0226e1003ef787fc7deb196525eab273cf3ccb152a89bcc77ad31c/68747470733a2f2f75706c6f61642e77696b696d656469612e6f72672f77696b6970656469612f636f6d6d6f6e732f642f64302f486173685f7461626c655f355f305f315f315f315f315f315f4c4c2e737667)

