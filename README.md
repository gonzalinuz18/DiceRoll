"# DiceRoll" 
package com.example.diceroller

import android.hardware.camera2.params.Face
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.os.Parcel
import android.os.Parcelable

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        main()
        val myFirstDice=Dice (6,"blue" )
        val diceRoll = myFirstDice.roll()
        val diceColor = myFirstDice.colors()
        val myCoin = Dice (1,"")


    }




    private fun main() {

        val myFirstDice =  Dice(6,"blue")
        println("your ${myFirstDice.numSides} sided dice rolled ${myFirstDice.roll()}!, and the color is ${myFirstDice.color1} ")

        val mySecondDice = Dice (20,"purple")
        println("your ${mySecondDice.numSides} sided dice rolled ${mySecondDice.roll()}!, and the color is ${mySecondDice.color1} ")

        val myThirdDice =  Dice(13,"red")
        println("your ${myFirstDice.numSides} sided dice rolled ${myThirdDice.roll()}!, and the color is ${myThirdDice.color1} ")

        val myCoin = Dice (2,"")
        println("the face of my coin is ${myCoin.roll()}! and the coin ${myCoin.roll()} is rolling")


    }
        class Dice(val numSides: Int, var color1:String="") {


            fun roll(): Int {
                return (1..numSides).random()
            }

            fun colors (){

               val color = color1

            }

        }


}
