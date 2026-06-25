=if(istext(N36),
if(M36 = "Melee Attack","+"&
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>0, VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)+$AC$106&
                                                     if($AI$106>0, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>1, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-5,) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>2, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-10,) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>3, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-15,)
,)&

if(M36 = "Ranged Attack",
   if($AJ$106>0, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)& " / ",) &
   if($AJ$106>1, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)& " / ",) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>0, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>1, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-5,) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>2, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-10,) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>3, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-15,)
,)&

if(M36 = "Off-Hand Melee Attack (must have TWF 1, 2, or 3 active on Buff Table)",
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>0, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>1, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-5,) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>2, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-10,) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>3, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-15,)
,)&

if(M36 = "Off-Hand Ranged Attack (must have TWF 1, 2, or 3 active on Buff Table)",
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>0, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>1, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-5,) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>2, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-10,) &
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>3, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-15,)
,)&

if(M36 = "Offensive Combat Maneuver",
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>0, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)+$AC$106,)
,)&

if(M36 = "Magic",
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>0, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)
,)&


if(M36 = "Flurry",
if(OR(arrayformula(regexmatch($AI$4,"Monk \(Unchained\)"))),

     if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>0, "+" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)+$AC$106,)&
                  if(AND($AJ$106>0,regexmatch(N36,"Ranged")), " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
                  if(AND($AJ$106>1,regexmatch(N36,"Ranged")), " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
                  if(AND($AJ$106>3,regexmatch(N36,"Ranged")), " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
                  if(AND($AI$106>0,regexmatch(N36,"Melee")), " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
     if(Vlookup("Monk (Unchained)",$AI$3:$AM$5,13,false)>0 , " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),) &
     if(Vlookup("Monk (Unchained)",$AI$3:$AM$5,13,false)>10, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),) &
     if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>1, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-5,) &
     if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>2, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-10,) &
     if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>3, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-15,)
    ,
     if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>0, "+" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)+$AC$106-2,)&
                  if(AND($AJ$106>0,regexmatch(N36,"Ranged")), " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-2,)&
                  if(AND($AJ$106>1,regexmatch(N36,"Ranged")), " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-2,)&
                  if(AND($AJ$106>3,regexmatch(N36,"Ranged")), " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-2,)&
                  if(AND($AI$106>0,regexmatch(N36,"Melee")), " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-2,)&
     if(Vlookup("Monk",$AI$3:$AM$5,13,false)>0 , " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-2,) &
     if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>1, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-7,) &
     if(Vlookup("Monk",$AI$3:$AM$5,13,false)>5 , " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-7,) &
     if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>2, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-12,) &
     if(Vlookup("Monk",$AI$3:$AM$5,13,false)>10 , " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-12,) &
     if(Vlookup("Monk",$AI$3:$AM$5,13,false)>15 , " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-17,)
),)&

if(M36 = "Single Attack",
   if(Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>0, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)+$AC$106,)
,)&


if(M36 = "Natural Attacks (Searches attack name for # of attacks, defaults to 1)",
                                   "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)+if(REGEXMATCH(N36,"Haste Applies"),$AC$106,)&
   if(AND(REGEXMATCH(N36,"Haste Applies"),$AI$106>0), " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
   if(REGEXMATCH(E36,"[2-9]+"), " / +"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
   if(REGEXMATCH(E36,"[3-9]+"), " / +"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
   if(REGEXMATCH(E36,"[4-9]+"), " / +"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
   if(REGEXMATCH(E36,"[5-9]+"), " / +"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
   if(REGEXMATCH(E36,"[6-9]+"), " / +"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)
,)&

if(
   M36 = "Other", 
   if(
      N36="Alchemist Bomb (DEX to hit, INT to damage) (No Rapid Bomb Discovery)",
      if(1+int(BaseAttack/5)>0, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)
      ,)&
   if(
      N36="Alchemist Bomb (DEX to hit, INT to damage) (Rapid Bomb)",
      if($AJ$106=1, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)& " / ",) &
      if($AJ$106=2, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)& " / ",) &
      if(1+int(BaseAttack/5)>0, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),) &
      if(1+int(BaseAttack/5)>1, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-5,) &
      if(1+int(BaseAttack/5)>2, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-10,) &
      if(1+int(BaseAttack/5)>3, " / +" & VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-15,)
      ,)&
   if(
      N36="Witch Prehensile Hair (INT to hit / INT to damage)",
      if(1+int(BaseAttack/5)>0, "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)+$AC$106,)
      ,)&

  if(REGEXMATCH(N36,"Kineticist"),
      if(REGEXMATCH(N36,"Ranged"), "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
      if(AND(REGEXMATCH(N36,"Melee"),Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>0),    "+"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)+$AC$106,)&
      if(AND(REGEXMATCH(N36,"Melee"),$AI$106>0),                                                   " / +"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36),)&
      if(AND(REGEXMATCH(N36,"Melee"),Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>1), " / +"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-5,)&
      if(AND(REGEXMATCH(N36,"Melee"),Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>2), " / +"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-10,)&
      if(AND(REGEXMATCH(N36,"Melee"),Vlookup(M36,INDIRECT('Formula References'!$B74),3,FALSE)>3), " / +"&VLOOKUP(N36,INDIRECT('Formula References'!$B74),2,False)+$B36+if($D36 = "MW", 1, $D36)-15,)
      ,)
  ,)
,)
