# bitbucket-cheat-sheet


# Branch


<details><summary>Click to expand..</summary>
  
<br><br>

### 🔐 Schritt-für-Schritt: Branch vor Direkt-Push schützen

<details><summary>Click to expand..</summary>

1. **Öffne dein Repository** in Bitbucket.
2. Gehe in der linken Navigation zu **Repository settings** *(ganz unten)*.
3. Klicke auf **Branch permissions** (unter *Workflow* oder *Workflow settings*).
4. Klicke auf **Add a branch permission**.

#### Konfiguriere die Rechte:

- **Branch name pattern**: z. B. `main`, `develop`, oder `release/*` – was du schützen willst.
- **Write access**: *Lass dieses Feld leer* oder gib nur ausgewählten Nutzern Zugriff.
- Aktiviere:  
  ✅ *Prevent all changes without a pull request* (oder sinngemäß: *Nur Änderungen via Pull Request zulassen*).

Optional kannst du auch:

- ✅ *Require pull request approvals* aktivieren (z. B. mindestens 1 Reviewer).
- ✅ *Prevent deletion* anhaken – damit keiner aus Versehen den Branch killt.

5. Klicke auf **Add** oder **Save**.

### Ergebnis:

Kein Push mehr direkt auf `main` oder `develop`. Jeder muss einen PR stellen und – je nach Einstellungen – Review durchlaufen. Ideal für saubere Git-Hygiene. 🧼💣

Willst du's per Bitbucket API oder in mehreren Repos automatisieren?


</details>


</details>

































<br><br>
________
________
<br><br>




# PR

<details><summary>Click to expand..</summary>



<br><br>


## FAQ

<details><summary>Click to expand..</summary>

### Warum sehe ich zwei Kommentare beim Mergen eines Pull-Requests?

In Bitbucket gibt es zwei separate "Events" beim Mergen eines Pull-Requests, die zu zwei Kommentaren führen können:

1. **Merge Commit:** Wenn der Pull-Request gemerged wird, erzeugt Bitbucket ein Commit, das den Merge-Prozess selbst widerspiegelt. Dieses Commit wird als Kommentar angezeigt (z.B. `Merged in docs/PRIV-48/jsdocs-hinzufuegen/main`).

2. **Vorheriger Commit:** Das letzte Commit in deinem Feature-Branch, das vor dem Merge gemacht wurde, bleibt ebenfalls sichtbar, da es der Code ist, der tatsächlich in den Ziel-Branch (z.B. `develop`) eingeführt wurde.

**Warum zwei Kommentare?**  
Das liegt daran, dass der Merge-Commit selbst ein separates Ereignis ist, und dein vorheriges Commit wird nicht durch den Merge entfernt oder verändert. Beide werden als separate Kommentare angezeigt, da es sich um unterschiedliche Aktionen im Versionskontrollprozess handelt.

Du kannst die Merge-Nachricht aus dem Pull-Request nicht direkt entfernen, aber sie stellt lediglich den Merge-Prozess dar und kann ignoriert werden.

</details>








<br><br>
<br><br>






## Bitbucket - Syntax-Highlighting für Pull-Requests aktivieren

1. Gehe zu [Bitbucket Account Settings](https://bitbucket.org/account/settings/features/).
2. Scrolle nach unten zu "Labs".
3. Aktiviere die Option "Syntax Highlighting for Pull Requests" unter den verfügbaren Labs-Features.

Damit werden Diffs in Pull-Requests mit Syntax-Highlighting angezeigt, was das Lesen von Codeunterschieden vereinfacht.

</details>























