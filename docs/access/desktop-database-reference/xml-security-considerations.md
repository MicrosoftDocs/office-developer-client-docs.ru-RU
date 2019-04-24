---
title: XML Security Considerations
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 648e7980be19f8af39cdb5e19858ba1ffd16518e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308248"
---
# <a name="xml-security-considerations"></a>Рекомендации по безопасности XML


**Область применения**: Access 2013, Office 2013

## <a name="xml-security-considerations"></a>XML Security Considerations

Методы **сохранения** и **открытия** ADO в объекте **Recordset** не считаются безопасными операциями для запуска в Internet Explorer. Таким образом, если эти методы используются в коде скрипта, который выполняется в приложении или элементе управления, размещенном в браузере, конфигурация безопасности браузера будет влиять на его поведение.

Internet Explorer 5 предоставляет ограничения безопасности для таких операций по умолчанию в зонах Интернета. В этой конфигурации **набор записей** не может осуществлять доступ к локальной файловой системе клиента или получать доступ к источникам данных вне домена сервера, с которого была загружена страница. В частности, при выполнении внутри узла браузера, объект **Recordset** можно сохранить обратно в файл только в том случае, если он находится на том же сервере, из которого была загружена страница. Аналогично, можно открыть объект **Recordset** , загрузив его из файла только в том случае, если этот файл находится на том же сервере, из которого была загружена страница.

Дополнительные сведения о безопасности в Internet Explorer можно найти в технической статье "вопросы безопасности ADO и RDS в Microsoft Internet Explorer".

