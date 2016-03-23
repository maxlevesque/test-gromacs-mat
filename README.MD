```sh
git clone https://github.com/maxlevesque/test-gromacs-mat
gmx grompp -f eql.mdp -o eql.tpr -c min.gro -p topol.top
gmx mdrun -ntomp 1 -ntmpi 4  -deffnm eql -v
```

Et les perfs affichée dans le stdout:

```sh
               Core t (s)   Wall t (s)        (%)
       Time:     2064.266      515.713      400.3
                 (ns/day)    (hour/ns)
Performance:      167.535        0.143
```

Le fichier de log est `eql.log`.
