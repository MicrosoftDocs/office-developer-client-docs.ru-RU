---
title: Объект Procedure (ADOX)
TOCTitle: Procedure object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72f0475aeca38b5c6ba6cd2954ff894f00fb6f7f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922652"
---
# <a name="procedure-object-adox"></a>Объект Procedure (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет хранимую процедуру. При использовании в сочетании с объектом ADO [команду](command-object-ado.md) объект **процедуры** можно использовать для добавления, удаления или изменения хранимые процедуры.

## <a name="remarks"></a>Примечания

Объект **процедуры** позволяет создавать хранимую процедуру без необходимости знать или используйте синтаксис «Создать процедуру» поставщика.

Свойства объекта **процедуры** можно выполнить следующие действия.

  - Определите процедуру с помощью свойства [Name](name-property-adox.md) .

  - Укажите объект ADO **команды** , который можно использовать для создания или выполнения процедуры с помощью свойства [команды](command-property-adox.md) .

  - Возвращает сведения о датах с помощью свойства [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .

