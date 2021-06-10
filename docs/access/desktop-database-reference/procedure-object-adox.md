---
title: Объект Procedure (ADOX)
TOCTitle: Procedure object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ad8f87aa78fbc05694fc53f0d4a55dce43315077
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301395"
---
# <a name="procedure-object-adox"></a>Объект Procedure (ADOX)


**Область применения**: Access 2013, Office 2013

Представляет сохраненную процедуру. При использовании в сочетании с объектом ADO [Command](command-object-ado.md) объект **Procedure** можно использовать для добавления, удаления или изменения сохраненных процедур.

## <a name="remarks"></a>Примечания

Объект **Procedure** позволяет создавать сохраненную процедуру без необходимости знать синтаксис "CREATE PROCEDURE" поставщика или использовать его.

Со свойствами объекта **Procedure** можно:

  - Определите процедуру с [свойством Name.](name-property-adox.md)

  - Укажите объект ADO **Command,** который можно использовать для создания или выполнения процедуры с помощью [свойства Command.](command-property-adox.md)

  - Сведения о дате возврата со свойствами [DateCreated](datecreated-property-adox.md) и [DateModified.](datemodified-property-adox.md)

