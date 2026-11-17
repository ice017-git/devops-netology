### Шаблоны gitignore

- `*.tfstate`, `*.tfstate.*`
  `*` — любая последовательность символов (включая пустую). Игнорируются все файлы, имя которых заканчивается на `.tfstate`, а также файлы, в имени которых встречается `.tfstate.` (например, `terraform.tfstate.backup`).

- `crash.log`, `crash.*.log`
  Первая строка — файл с точным именем `crash.log`. Вторая — файлы вида `crash.<что угодно>.log`.

- `*.tfvars`, `*.tfvars.json`
  Все файлы с расширением `.tfvars` и `.tfvars.json`.

- `override.tf`, `override.tf.json`, `*_override.tf`, `*_override.tf.json`
  Первые две строки — точные имена. Остальные — любые файлы, имя которых заканчивается на `_override.tf` или `_override.tf.json`.

- `.terraform/`
  Слэш на конце означает: правило применяется только к каталогу с именем `.terraform` (и всему его содержимому), но не к файлу с таким именем.

- `.terraform.tfstate.lock.info`
  Файл с точным именем.

- `.terraformrc`, `terraform.rc`
  Файлы с точными именами.

- `*.dot`, `planout`  (закомментированы)
  `*.dot` — все файлы с расширением `.dot`; `planout` — файл с точным именем `planout`.
