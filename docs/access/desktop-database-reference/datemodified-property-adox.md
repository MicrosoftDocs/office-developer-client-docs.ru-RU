---
title: DateModified Property (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceafd13b33536a77a1d793e7167fe8042609be5e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603331"
---
# <a name="datemodified-property-adox"></a>DateModified Property (ADOX)


**Применимо к**: Access 2013 | Office 2013

Указывает дату последнего изменения объекта.

<<<<<<< HEAD
## <a name="return-values"></a>Return Values
=======
## <a name="return-values"></a>Возвращаемые значения
>>>>>>> master

Возвращает значение **типа Variant** , указав дату изменения. Значение null, если **DateModified** не поддерживается поставщиком.

## <a name="remarks"></a>Замечания

Свойство **DateModified** имеет значение null для добавленного объектов. После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateModified** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .

