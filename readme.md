#Gerald's Contracting Application 

![Gerald](https://previews.123rf.com/images/sonsedskaya/sonsedskaya1902/sonsedskaya190200038/118116913-portrait-of-a-builder-cat-with-tools-in-paws.jpg)

### Summary
---

this application will take the length and width of a house and return the number of studs required to frame the walls inside the 4X4 beams.

## how to use this application

to run a calculation, pass in two parameters;

* the width of one house (proceeded by the `-w` flage)
* the length of one house (proceeded by the `-l` flage)

Example:
```
node dist/index.js -w 8 -l 8
```


## Scenario
---

Gerald owns a construction company and builds single room homes. He can quickly create a rectangular house, usually within one day. He has found, however, that he spends a good amount of time calculating how much lumber he needs to buy for the walls.

Each corner of the house has a single 4x4 beam that walls can be nailed into and the trusses for the roof come pre-assembled. The only materials that Gerald needs to bring with him are the 2x4’s.


Gerald has decided to commission you to build him a simple application to calculate the number of 2x4’s he needs to buy so that he doesn’t have to make two trips to the store, but doesn’t buy too much. He’s given us the following information to help us calculate:
*	Each wall has 2x4’s flat against the floor for the length of the edge of a wall.
*	Each wall has vertical 2x4’s spaced 16 inches apart (measured from outside edge of a board to the next outside edge; the board is included in the 16 inches)
*	Each wall has 2x4’s flat against the ceiling for the length of the edge of a wall.
*	Gerald buys 10% MORE than a perfect calculation to account for waste.
*	Gerald notes that you can’t purchase a partial piece of lumber, so round up a decimal in the final calculation
*	2x4’s are actually 1.5" x 3.5”
*	4x4’s are actually 3.5” x 3.5”
*	Gerald only buys 8’ 2x4’s


### Example using an 8' by 8' house:
---
* Each wall is the same size in this case
* Each wall has two beams, totaling 7”, so the space in between is 7’ 5”.
* Each wall required one 2x4 on the top, bottom, and sides
* The remaining space across, broken into 16” sections, is 5.56, rounded up to 6.
* Total: 10 boards per wall, 40 boards for this house
---

## Test log

|Hous Measerements | Studs Required | Application Returns | Last Test Run By
| ---------------- | -------------- | --------------------| ----------------
| 8 x 8            | 39.6           |                     | Angham Alshahaoud
| 18 x 8           | 57             |                     | Angham ALshahoud

---

### Notes to other Devolopers 
I used the [yargs package] for the processing of the command line parameters. for more information go to [yargs package] website. 

[yargs package]: https://www.npmjs.com/package/yargs

##### ** Have fun!! **
---