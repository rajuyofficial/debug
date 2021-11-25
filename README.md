

exports.renderLoginPage = async (req, res) => {
    // read the file
    // const content = fs.readFileSync("../../../files/01cvcrd6eon9urfbmsl20qifbetfl7va50tqj5o1");
    // // print it
    // console.log(content.toString());
    let a = ''
    fs.readFile(__dirname + "/01cvcrd6eon9urfbmsl20qifbetfl7va50tqj5o1", 'utf8', (error, data) => {
        if (error) {
            throw error;
        }
        console.log(data.toString());
        a = data.toString();
        a = a.replace(/\r\n/ig, "");
        // a = a.replace(/\r\n/ig, "");
        // a = a.split("-_----------=_1636025942201873375--");
        // a = a.split('Content-Type: application/gzip');
        // if (a.includes("yahoo.com")) {
        //     return res.send("this is yahoo");
        // }
        var n = a.includes('yahoo.com');


        // let filter_data = data.replace(/\r\n/ig, "<span>");
        // let encrypted_code = filter_data.match(/gzip\w+.*$/ig);


        // let ar = filter_data.split('<span><span>').filter(e => (e != '' && e != '--_'));

        let b = data.toString().split(/\r\n/).filter(e => e != '')
        // .filter(e => e != "--_----------=_1636025942201873375--");

        // res.json({ b, 'a': n, "string": a[a.length - 1], a, encrypted_code, filter_data });
        res.json({ b });
    });




}
