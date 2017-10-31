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

### Instructions

1. Launch this URL in a browser: https://bencompton.github.io/text-to-jasmine/

2. Paste your scenario text into the first box

3. Click "Convert"

4. Copy your generated code from the second box and paste into your code editor

### Notes

This utility expects your scenario text to have each description (describe block) and assertion (it block) on a separate line, and the assertion should have a dash in front of it:

```
Description
	-Assertion
```

Also, only tab indents are supported at the moment, but space indent support may be added later. The output code will also use tab indents.
