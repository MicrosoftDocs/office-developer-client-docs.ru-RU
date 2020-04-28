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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294409"
---
# <a name="datemodified-property-adox"></a>Свойство DateModified (ADOX)


**Область применения**: Access 2013, Office 2013

Указывает дату последнего изменения объекта.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение **типа Variant** , указывающее дату изменения. Значение равно null, если **DateModified** не поддерживается поставщиком.

## <a name="remarks"></a>Примечания

Для новых добавленных объектов свойство **DateModified** имеет значение null. После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md)необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции [представлений](views-collection-adox.md) или [процедур](procedures-collection-adox.md) для получения значений для свойства **DateModified** .

