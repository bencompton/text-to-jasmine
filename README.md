# Convert scenario text into Jasmine / Mocha code

This utility will automatically convert scenario text you have written in a text editor like this:

```
When I have some scenario text
  -should convert it into code
  When I have a nested describe block
    -should also convert that to code
When I have multiple describe blocks
  -should be converted into code too
```

Into Jasmine / Mocha code like this:

```javascript
describe('When I have some scenario text', () => {
    it('should convert it into code');
    describe('When I have a nested describe block', () => {
        it('should also convert that to code');
    });
});
describe('When I have multiple describe blocks', () => {
    it('should be converted into code too');
});
```
