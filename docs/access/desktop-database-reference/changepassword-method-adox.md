---
title: Метод ChangePassword (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296530"
---
# <a name="changepassword-method-adox"></a>Метод ChangePassword (ADOX)

**Область применения**: Access 2013, Office 2013

Изменяет пароль для учетной записи пользователя.

## <a name="syntax"></a>Синтаксис

*User (пользователь*). ChangePassword*олдпассворд*, *newPassword*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Олдпассворд* |**Строковое** значение, задающее существующий пароль пользователя. Если у пользователя в данный момент нет пароля, используйте пустую строку ("") для *олдпассворд*.|
|*NewPassword* |**Строковое** значение, задающее новый пароль.|

## <a name="remarks"></a>Замечания

В целях безопасности необходимо указать старый пароль в дополнение к новому паролю.

Если поставщик не поддерживает администрирование свойств доверенного лица, произойдет ошибка.

