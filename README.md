# BV4J #

BV4J is a library for reading EEG data in BrainVision format. It supports the import of selected channels and epochs.

### Features ###
* reads data in binary format (no ASCII yet)
* MULTIPLEXED or VECTORIZED data orientation
* 16-bit integer, 32-bit float or 64-bit double data types

### Example usage ###
	File file = new File("somePathToHeaderFile.vhdr")
	BrainVisionReader bv = new BrainVisionReader(file);
	int channel = 0; int from = 0; int to = 3000; //reads content of first channel from sample 0 to 3000 (inclusive)
	bv.read(channel, from, to);
	float[] data = bv.getData();
	bv.close();


### Bugs & Suggestions ###
If you find bugs or have suggestions regarding parts of the software, please file a [report/request](https://github.com/xuser/bv4j/issues) on GitHub or [email](weigenand@inb.uni-luebeck.de) me.


