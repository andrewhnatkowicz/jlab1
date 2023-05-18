// ==UserScript==
// @name           Jlab Cheater
// @description    jlab cheat (fake results to print and give your teacher ;) )
// @include        http://education.jlab.org/solquiz/results.php*
// @version 0.0.1.20140525024113
// @namespace https://greasyfork.org/users/2178
// ==/UserScript==
var NumOfQs = document.getElementsByClassName('resultquestion').length
var oC=document.getElementsByClassName('resultincorrect').length
var oR=document.getElementsByClassName('resultcorrect').length
for (var i=1;i<NumOfQs;i++) {
	if (!document.getElementsByClassName('resultincorrect')){
		break;
	}
	if (document.getElementsByClassName('resultincorrect').length!=0){
		document.getElementsByClassName('resultincorrect')[0].innerHTML='Correct!';
		document.getElementsByClassName('resultincorrect')[0].setAttribute('class','resultcorrect');
	}
}
document.getElementsByClassName('sectionscore1')[0].innerHTML='You answered '+NumOfQs+' questions out of '+NumOfQs+' correctly!';
document.getElementsByClassName('sectionscore2')[0].innerHTML='Score for this section: 100.00%';
document.getElementById('totalscore').innerHTML='Total Score: 100.00%';
document.getElementById('timeindex').contentEditable='true';
