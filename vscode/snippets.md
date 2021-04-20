# Snippets de desenvolvimento

{
	"debug": {
		"prefix": "debug",
		"body": "echo '<pre>'; print_r($1); echo '</pre>';",
		"description": "Debug"
	},
	"debug com exit": {
		"prefix": "debuge",
		"body": "echo '<pre>'; print_r($1); echo '</pre>'; exit;",
		"description": "Debug com exit"
	},
	"test": {
		"prefix": "test",
		"body": "if(isset(\\$_GET['test'])){\r\n $1\r\n}",
		"description": "teste test"
	},
	"testX":{
		"prefix": "testX",
		"body": "if(isset(\\$_GET['test'])){\r\n echo '<pre>Init >><br/>';\r\nprint_r(\\$_POST);\r\necho '<br/>Type >><br/>'; \r\nvar_dump(\\$_POST); \r\necho '<br/>Backtrace >><br/>'; \r\nvar_dump(debug_backtrace()); \r\nprint_r(debug_backtrace());\r\necho '</pre>'; \r\nexit('Teste close'); \r\n}"
	},
	"debugeX": {
		"prefix":"debugeX",
		"body":"echo '<pre>';\r\nprint_r(\\$_POST);\r\necho '<br/>Type >><br/>'; \r\nvar_dump(\\$_POST); \r\necho '<br/>Backtrace >><br/>'; \r\nvar_dump(debug_backtrace()); \r\nprint_r(debug_backtrace());\r\necho '</pre>'; \r\nexit('Teste close');"
	},
	"get-errors": {
		"prefix": "display_errors",
		"body": "ini_set(\"display_errors\", true);\r\nerror_reporting(E_ALL);",
		"description": "Disyplay errors"
	},
	"Benchmark": {
		"prefix": "benchmark",
		"body": "define('START', microtime(true));\r\nregister_shutdown_function(function(){\r\n \\$time = microtime(true) - START;\r\n echo '<pre>'; print_r(number_format(\\$time, 6)); echo '</pre>'; exit;\r\n});",
		"description": "Benchmark"
	}
}
