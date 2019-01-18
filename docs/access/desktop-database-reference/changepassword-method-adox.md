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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713095"
---
# <a name="changepassword-method-adox"></a>Метод ChangePassword (ADOX)

**Применимо к**: Access 2013, Office 2013

Изменение пароля для учетной записи пользователя.

## <a name="syntax"></a>Синтаксис

*Пользователь*. Изменение пароля*Старый_пароль*, *Новый_пароль*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Старый_пароль* |**Строковое** значение, задающее существующий пароль пользователя. Если у пользователя нет в настоящее время пароль, укажите пустую строку ("») для *Старый_пароль*.|
|*Новый_пароль* |**Строковое** значение, задающее новый пароль.|

## <a name="remarks"></a>Замечания

По соображениям безопасности старый пароль должен быть указан в дополнение к новый пароль.

Если поставщик поддерживает администрирования свойства доверенного лица, произойдет ошибка.

