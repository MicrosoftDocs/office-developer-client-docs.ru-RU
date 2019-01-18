---
title: Свойство DateModified (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: daf72804d51c18b5875e607ce5fdb0dfe20f406c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726080"
---
# <a name="datemodified-property-adox"></a>Свойство DateModified (ADOX)


**Применимо к**: Access 2013, Office 2013

Указывает дату последнего изменения объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение **типа Variant** , указав дату изменения. Значение null, если **DateModified** не поддерживается поставщиком.

## <a name="remarks"></a>Замечания

Свойство **DateModified** имеет значение null для добавленного объектов. После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateModified** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .

