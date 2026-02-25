DevOps course homework repository for netology

Файл .gitignore используется для игнорирования временных файлов Terraform,
локальныхсостояний инфраструктуры, файлов планов выполнения и секретов.


скриншоты
![1](https://github.com/mteplov/devops-netology/blob/main/1.png)
![2](https://github.com/mteplov/devops-netology/blob/main/2.png)



в конктреном случаии будут игнорироваться 
# Расшифровка правил Terraform .gitignore

## .terraform/
Игнорируется каталог с именем `.terraform` в текущей директории и всё его содержимое полностью, включая вложенные файлы и подкаталоги.

Примеры:
.terraform/providers/...
.terraform/modules/...
.terraform/terraform.tfstate


## *.tfstate
Игнорируются все файлы, имя которых заканчивается на `.tfstate`.

Примеры:
terraform.tfstate
prod.tfstate
dev.tfstate


## *.tfstate.*
Игнорируются файлы, имя которых:
- начинается с любого набора символов,
- содержит `.tfstate.`,
- и имеет любое продолжение после последней точки.

Примеры:
terraform.tfstate.backup
prod.tfstate.12345
dev.tfstate.old


## crash.log
Игнорируется файл строго с именем:
crash.log


## crash.*.log
Игнорируются файлы, имя которых:
- начинается с `crash.`,
- далее содержит любую последовательность символов,
- и заканчивается на `.log`.

Примеры:
crash.20240101.log
crash.error.log
crash.abc123.log

Не игнорируются:
crash.log
mycrash.1.log
crash.txt


## *.tfvars
Игнорируются все файлы, имя которых заканчивается на `.tfvars`.

Примеры:
terraform.tfvars
prod.tfvars
dev.tfvars


## *.tfvars.json
Игнорируются все файлы, имя которых заканчивается на `.tfvars.json`.

Примеры:
terraform.tfvars.json
prod.tfvars.json


## override.tf
Игнорируется файл строго с именем:
override.tf


## override.tf.json
Игнорируется файл строго с именем:
override.tf.json


## *_override.tf
Игнорируются файлы, имя которых заканчивается на `_override.tf`.

Примеры:
prod_override.tf
dev_override.tf
test_override.tf


## *_override.tf.json
Игнорируются файлы, имя которых заканчивается на `_override.tf.json`.

Примеры:
prod_override.tf.json
dev_override.tf.json


## .terraform.tfstate.lock.info
Игнорируется файл строго с именем:
.terraform.tfstate.lock.info


## .terraformrc
Игнорируется файл:
.terraformrc


## terraform.rc
Игнорируется файл:
terraform.rc

