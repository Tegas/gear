/script u=UnitMana('Player'); c=CastSpellByName; f=UnitPowerType("Player"); if (u<=30) and (f==3) then c"Cat Form"; elseif (f==0) then c"Cat Form"; end; 

/run for i = 1, GetNumShapeshiftForms() do local _, _, active = GetShapeshiftFormInfo(i) if active then CastShapeshiftForm(i) return end end

/run local _, _, active = GetShapeshiftFormInfo(3) if not active or IsControlKeyDown() then CastShapeshiftForm(3) else CastSpellByName"Prowl" end

/run local _, _, active = GetShapeshiftFormInfo(1) if not active or IsControlKeyDown() then for i = 2, 4 do _, _, active = GetShapeshiftFormInfo(i) if active then CastShapeshiftForm(i) return end end CastShapeshiftForm(1) else CastSpellByName"Bash" end

/run if GetComboPoints()>=5 then CastSpellByName("Ferocious Bite") else CastSpellByName("Claw") end
/script if GetComboPoints()>=5 then CastSpellByName("Eviscerate") else CastSpellByName("Sinister Strike") end


/run i=0 m=0 c=CastSpellByName while not (GetPlayerBuff(i)==-1) do if (strfind(GetPlayerBuffTexture(GetPlayerBuff(i)),"Ability_Mount_JungleTiger")) then m=1 end i=i+1 end if m==0 then c("Tiger's Fury") else c("Ravage") end


/run c=CastSpellByName function b(k)for i=1,16 do if strfind(tostring(UnitDebuff("target",i)),k)then return 1 end end end if not b("e_FaerieF")then c("Faerie Fire(Rank 4)")elseif not b("e_InsectSw")then c("Insect Swarm(Rank 1)")end


/run
if GetComboPoints()>=5 then
	CastSpellByName("Ferocious Bite")
elseif 
else
	CastSpellByName("Claw")
end

/script
u=UnitMana('Player');
c=CastSpellByName;
f=UnitPowerType("Player");
if (GetComboPoints()>=5) then
	c"Ferocious Bite";
elseif (u<=30) and (f==3) and IsControlKeyDown() then
	c"Cat Form";
elseif (f==0) then
	c"Claw";
end;




/script u=UnitMana('Player'); c=CastSpellByName; f=UnitPowerType("Player"); if (u<=30) and (f==3) then c"Cat Form"; elseif (f==0) then c"Cat Form"; end; 


