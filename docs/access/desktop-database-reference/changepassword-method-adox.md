---
title: Изменение пароля метод (ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 34de673d29d160c715c8e2617d0e2a75e3843904
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872237"
---
# <a name="changepassword-method-adox"></a>Изменение пароля метод (ADOX)


**Применимо к**: Access 2013, Office 2013



Изменение пароля для учетной записи пользователя.

## <a name="syntax"></a>Синтаксис

*Пользователь*. Изменение пароля*Старый_пароль*, *Новый_пароль*

## <a name="parameters"></a>Параметры

  - *Старый_пароль*

  - **Строковое** значение, задающее существующий пароль пользователя. Если у пользователя нет в настоящее время пароль, укажите пустую строку ("») для *Старый_пароль*.

  - *Новый_пароль*

  - **Строковое** значение, задающее новый пароль.

## <a name="remarks"></a>Замечания

По соображениям безопасности старый пароль должен быть указан в дополнение к новый пароль.

Если поставщик поддерживает администрирования свойства доверенного лица, произойдет ошибка.

