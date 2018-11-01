---
title: Объект процедуры (ADOX)
TOCTitle: Procedure Object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: afc4eae76395e7a15573ad5343955b0ab46df3db
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883353"
---
# <a name="procedure-object-adox"></a><span data-ttu-id="25233-102">Объект процедуры (ADOX)</span><span class="sxs-lookup"><span data-stu-id="25233-102">Procedure Object (ADOX)</span></span>


<span data-ttu-id="25233-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="25233-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25233-104">Представляет хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="25233-104">Represents a stored procedure.</span></span> <span data-ttu-id="25233-105">При использовании в сочетании с объектом ADO [команду](command-object-ado.md) объект **процедуры** можно использовать для добавления, удаления или изменения хранимые процедуры.</span><span class="sxs-lookup"><span data-stu-id="25233-105">When used in conjunction with the ADO [Command](command-object-ado.md) object, the **Procedure** object can be used for adding, deleting, or modifying stored procedures.</span></span>

## <a name="remarks"></a><span data-ttu-id="25233-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="25233-106">Remarks</span></span>

<span data-ttu-id="25233-107">Объект **процедуры** позволяет создавать хранимую процедуру без необходимости знать или используйте синтаксис «Создать процедуру» поставщика.</span><span class="sxs-lookup"><span data-stu-id="25233-107">The **Procedure** object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</span></span>

<span data-ttu-id="25233-108">Свойства объекта **процедуры** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="25233-108">With the properties of a **Procedure** object, you can:</span></span>

  - <span data-ttu-id="25233-109">Определите процедуру с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="25233-109">Identify the procedure with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="25233-110">Укажите объект ADO **команды** , который можно использовать для создания или выполнения процедуры с помощью свойства [команды](command-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="25233-110">Specify the ADO **Command** object that can be used to create or execute the procedure with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="25233-111">Возвращает сведения о датах с помощью свойства [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="25233-111">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

