### Promise

~~~
// 2018-03-04 雏形
function Promise(fn) {
	var status = 'pending'

	function resolve() {
		status = 'resolve'
		successArray.forEach(node => { node.apply(undefined, arguments) })
	}
	function reject() {
		status = 'reject'
		failArray.forEach(node => { node.apply(undefined, arguments) })
	}

	let [successArray,failArray] = [[],[]]

	fn.call(undefined,resolve,reject)

	return {
		then: function (successFn,failFn){
			successArray.push(successFn)
			failArray.push(failFn)
			return undefined
		}
	}

}

var p = Promise(function(resolve,reject) { 
	setTimeout(function(){
		resolve('成功')
	},1000)
})

p.then((res)=>{
	console.log(res) //'成功'
})
~~~
