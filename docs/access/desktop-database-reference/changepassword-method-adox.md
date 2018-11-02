---
title: Метод ChangePassword (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f11cfaddc99a0e10a86e0df9a7a187c4e89fc794
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921063"
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

