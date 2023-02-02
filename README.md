# Learning about The sigmoid function

Elemental javascript perceptron


![Gjl-t(x)](https://user-images.githubusercontent.com/89952475/216314168-1946b718-ebda-40f7-b1fe-ff4f1095f81f.svg)


```
  var neuro = function() {
         
        this._seed = 1;
        this._threshold = 1;
        this._bias = 1;
        this._learnRate = 0.1;
        this._weights = [];
        this._neuralData = [];
    };
 
    neuro.prototype._random = function() {
        var x = Math.sin(this._seed++) * 10000;
        return x - Math.floor(x);
    };
 
    neuro.prototype._multiply = function (inputs) {
        var result = 0;
 
        for (var i = 0; i &amp;lt; inputs.length; i++) {
            result += inputs[i] * this._weights[i];
        }
 
        result += this._threshold * this._weights[this._weights.length - 1];
 
        return result;
    },
 
    neuro.prototype._sigmoid = function(x) {
        return 1 / (1 + Math.pow(Math.E, -x));
    };
  


```
