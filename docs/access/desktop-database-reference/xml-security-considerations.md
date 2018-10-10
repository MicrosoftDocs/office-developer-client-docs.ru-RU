---
title: XML Security Considerations
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3120db77ba89aee1036de4d6fa85df73c21d26d9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482429"
---
# <a name="xml-security-considerations"></a>XML Security Considerations


**Применимо к**: Access 2013 | Office 2013

## <a name="xml-security-considerations"></a>XML Security Considerations

Методы ADO **сохранения** и **открытия** в объекте **набора записей** , не считаются безопасных операций для запуска в Internet Explorer. Таким образом Если эти методы используются в коде скрипта, который работает в приложения или элемента управления, которая размещается в браузере, настройка безопасности обозревателя будут иметь влияет на поведение.

Internet Explorer 5 обеспечивает ограничения безопасности для таких операций по умолчанию в зоне Интернета. В разделе этой конфигурации **набора записей** невозможно сделать никакого доступа к локальной файловой системе на стороне клиента или получить доступ к источникам данных за пределами домена сервера, из которой был загружен страницы. В частности при выполнении внутри узла браузера **записей** можно сохранить обратно в файл только в том случае, если это на том же сервере, из которой был загружен страницы. Аналогично можно открыть **записей** путем загрузки из файла, только если этот файл находится на том же сервере, из которой был загружен страницы.

Дополнительные сведения о безопасности в Internet Explorer см «ADO и проблемы безопасности служб удаленных рабочих СТОЛОВ в Microsoft Internet Explorer.»

