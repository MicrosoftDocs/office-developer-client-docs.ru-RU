---
title: Метод ChangePassword (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7eef5fc93f9cce68e6342b62c1ab07ee6f65587f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946022"
---
# <a name="changepassword-method-adox"></a>Метод ChangePassword (ADOX)


**Применимо к**: Access 2013, Office 2013



Изменение пароля для учетной записи пользователя.

## <a name="syntax"></a>Синтаксис

*Пользователь*. Изменение пароля*Старый_пароль*, *Новый_пароль*

## <a name="parameters"></a>Параметры

- *Старый_пароль*

  - **Строковое** значение, задающее существующий пароль пользователя. Если у пользователя нет в настоящее время пароль, укажите пустую строку ("») для *Старый_пароль*.

- *Новый_пароль*

  - **Строковое** значение, задающее новый пароль.

## <a name="remarks"></a>Примечания

По соображениям безопасности старый пароль должен быть указан в дополнение к новый пароль.

Если поставщик поддерживает администрирования свойства доверенного лица, произойдет ошибка.

