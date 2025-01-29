- En el paso 11 he usado el comando git reset --hard HEAD~1, ya que así deshago mi último commit y elimino los cambios también en el working area.
- En el paso 12 he usado el comando git reflog, en el que me desplazo hasta el hash donde creo mi segundo y último commit para poder deshacer el último paso.
Pero se me queda el commit sin asociar en ninguna rama, por lo que uso el comando git cherry-pick para tenerlo en mi rama styled.
- El merge del paso 13 no causó ningun conflicto.
-El merge del paso 19 causó el siguiente conflicto jmari@LAPTOP-T6IVH9VC MINGW64 ~/Documents/Practica-Git (styled)
$ git merge htmlify
Auto-merging git-nuestro.md
CONFLICT (content): Merge conflict in git-nuestro.md
Automatic merge failed; fix conflicts and then commit the result.
Aqui elimino los marcadores  >>>>>, ====, <<<<< con nano, luego añado a staging area y finalizo commiteando la resolución del conflicto.
-El merge del paso 21 no causó ningún conflicto.
-En el paso 25 usé el comando git log --oneline --graph --decorate --all
- El merge si podria haber sido fast forwards ya que previamente habiamos hecho un merge de main sobre styled dejando asi la vía “libre “ de commits entre main y title.
- En el paso 27 usé el comando git reset --merge
-En el paso 28 usé el comando git reset --hard HEAD~1
-En el paso 29 usé el comando git branch  -d
-En el paso 30 usé el comando git merge --no-ff title -m"Rehago el merge no fast-forward de title en main"
- En el paso 32 usé el comando git reset --hard <hash del primer commit>
-En el paso 33 usé el reflog para ver el hash del commit final y después el comando  git reset --hard<hash del primer commit>
