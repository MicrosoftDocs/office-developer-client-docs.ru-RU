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
# <a name="procedure-object-adox"></a><span data-ttu-id="312b5-102">Объект Procedure (ADOX)</span><span class="sxs-lookup"><span data-stu-id="312b5-102">Procedure object (ADOX)</span></span>


<span data-ttu-id="312b5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="312b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="312b5-104">Представляет хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="312b5-104">Represents a stored procedure.</span></span> <span data-ttu-id="312b5-105">При использовании в сочетании с объектом ADO [команду](command-object-ado.md) объект **процедуры** можно использовать для добавления, удаления или изменения хранимые процедуры.</span><span class="sxs-lookup"><span data-stu-id="312b5-105">When used in conjunction with the ADO [Command](command-object-ado.md) object, the **Procedure** object can be used for adding, deleting, or modifying stored procedures.</span></span>

## <a name="remarks"></a><span data-ttu-id="312b5-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="312b5-106">Remarks</span></span>

<span data-ttu-id="312b5-107">Объект **процедуры** позволяет создавать хранимую процедуру без необходимости знать или используйте синтаксис «Создать процедуру» поставщика.</span><span class="sxs-lookup"><span data-stu-id="312b5-107">The **Procedure** object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</span></span>

<span data-ttu-id="312b5-108">Свойства объекта **процедуры** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="312b5-108">With the properties of a **Procedure** object, you can:</span></span>

  - <span data-ttu-id="312b5-109">Определите процедуру с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="312b5-109">Identify the procedure with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="312b5-110">Укажите объект ADO **команды** , который можно использовать для создания или выполнения процедуры с помощью свойства [команды](command-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="312b5-110">Specify the ADO **Command** object that can be used to create or execute the procedure with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="312b5-111">Возвращает сведения о датах с помощью свойства [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="312b5-111">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

