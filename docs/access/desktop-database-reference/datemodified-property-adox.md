---
title: DateModified Property (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8465f97565d8519196b8221089121670ceedb275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480102"
---
# <a name="datemodified-property-adox"></a>DateModified Property (ADOX)


**Применимо к**: Access 2013 | Office 2013

Указывает дату последнего изменения объекта.

## <a name="return-values"></a>Return Values

Возвращает значение **типа Variant** , указав дату изменения. Значение null, если **DateModified** не поддерживается поставщиком.

## <a name="remarks"></a>Замечания

Свойство **DateModified** имеет значение null для добавленного объектов. После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateModified** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .

