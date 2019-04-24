---
title: Объект PROCEDURE (ADOX)
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
# <a name="procedure-object-adox"></a>Объект PROCEDURE (ADOX)


**Область применения**: Access 2013, Office 2013

Представляет хранимую процедуру. При использовании в сочетании с объектом [Command](command-object-ado.md) ADO объект **PROCEDURE** можно использовать для добавления, удаления или изменения хранимых процедур.

## <a name="remarks"></a>Замечания

Объект **PROCEDURE** позволяет создать хранимую процедуру без необходимости знать или использовать синтаксис поставщика "CREATE PROCEDURE".

С помощью свойств объекта **PROCEDURE** можно выполнить следующие действия:

  - Определите процедуру с помощью свойства [Name](name-property-adox.md) .

  - Укажите объект **команды** ADO, который можно использовать для создания или выполнения процедуры с помощью свойства [Command](command-property-adox.md) .

  - Сведения о дате возврата с помощью свойств [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .

