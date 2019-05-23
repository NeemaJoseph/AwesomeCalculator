# AwesomeCalculator
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using AwesomeCalculator;
using NUnit.Framework;

namespace CalculatorTest
{
    [TestFixture]
    class CalcTests
    {
        [Test]
        public void GetAddition_Input100point5and524point7_Return625point2()
        {
            //Arange
            double number1 = 100.5;
            double number2 = 524.7;

            double expectedResult = number1 + number2;

            Calc testCalc = new Calc(number1, number2);

            //Act
            double actualResult = testCalc.GetAddition();

            //Assert
            Assert.AreEqual(expectedResult, actualResult);
        }

        [Test]
        public void GetAddition_InputNegative1point2andNegative6point3_ReturnNegative7point5()
        {
            //Arange
            double number1 = -1.2;
            double number2 = -6.3;

            double expectedResult = number1 + number2;

            Calc testCalc = new Calc(number1, number2);

            //Act
            double actualResult = testCalc.GetAddition();

            //Assert
            Assert.AreEqual(expectedResult, actualResult);
        }

        [Test]
        public void GetAddition_InputNegative4andPositive5_ReturnPositive5()
        {
            //Arange
            double number1 = 4;
            double number2 = 5;

            double expectedResult = number1 + number2;

            Calc testCalc = new Calc(number1, number2);

            //Act
            double actualResult = testCalc.GetAddition();

            //Assert
            Assert.AreEqual(expectedResult, actualResult);
        }
