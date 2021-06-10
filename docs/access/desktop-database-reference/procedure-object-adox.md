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
# <a name="procedure-object-adox"></a><span data-ttu-id="90c2b-102">Объект Procedure (ADOX)</span><span class="sxs-lookup"><span data-stu-id="90c2b-102">Procedure object (ADOX)</span></span>


<span data-ttu-id="90c2b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="90c2b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90c2b-104">Представляет сохраненную процедуру.</span><span class="sxs-lookup"><span data-stu-id="90c2b-104">Represents a stored procedure.</span></span> <span data-ttu-id="90c2b-105">При использовании в сочетании с объектом ADO [Command](command-object-ado.md) объект **Procedure** можно использовать для добавления, удаления или изменения сохраненных процедур.</span><span class="sxs-lookup"><span data-stu-id="90c2b-105">When used in conjunction with the ADO [Command](command-object-ado.md) object, the **Procedure** object can be used for adding, deleting, or modifying stored procedures.</span></span>

## <a name="remarks"></a><span data-ttu-id="90c2b-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="90c2b-106">Remarks</span></span>

<span data-ttu-id="90c2b-107">Объект **Procedure** позволяет создавать сохраненную процедуру без необходимости знать синтаксис "CREATE PROCEDURE" поставщика или использовать его.</span><span class="sxs-lookup"><span data-stu-id="90c2b-107">The **Procedure** object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</span></span>

<span data-ttu-id="90c2b-108">Со свойствами объекта **Procedure** можно:</span><span class="sxs-lookup"><span data-stu-id="90c2b-108">With the properties of a **Procedure** object, you can:</span></span>

  - <span data-ttu-id="90c2b-109">Определите процедуру с [свойством Name.](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="90c2b-109">Identify the procedure with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="90c2b-110">Укажите объект ADO **Command,** который можно использовать для создания или выполнения процедуры с помощью [свойства Command.](command-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="90c2b-110">Specify the ADO **Command** object that can be used to create or execute the procedure with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="90c2b-111">Сведения о дате возврата со свойствами [DateCreated](datecreated-property-adox.md) и [DateModified.](datemodified-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="90c2b-111">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

