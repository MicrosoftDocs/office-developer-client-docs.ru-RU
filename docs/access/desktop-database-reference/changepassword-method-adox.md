---
title: ChangePassword Method (ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bd2f5d87c6f90e940858ce5c6e01099c5e539d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480107"
---
# <a name="changepassword-method-adox"></a>ChangePassword Method (ADOX)


**Применимо к**: Access 2013 | Office 2013



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

