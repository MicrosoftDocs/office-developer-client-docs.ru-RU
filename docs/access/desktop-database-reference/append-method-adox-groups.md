---
title: Метод Append (коллекция Groups в ADOX)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dfc2da5490cf5c148d39670dedfb2551cedd31f2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923590"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="40860-102">Метод Append (коллекция Groups в ADOX)</span><span class="sxs-lookup"><span data-stu-id="40860-102">Append method (ADOX Groups)</span></span>


<span data-ttu-id="40860-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="40860-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="40860-104">Добавляет новый объект [групповой](group-object-adox.md) в коллекцию [групп](groups-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="40860-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="40860-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40860-105">Syntax</span></span>

<span data-ttu-id="40860-106">*Группы*. Добавление*группы*</span><span class="sxs-lookup"><span data-stu-id="40860-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="40860-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="40860-107">Parameters</span></span>

  - <span data-ttu-id="40860-108">*group*</span><span class="sxs-lookup"><span data-stu-id="40860-108">*Group*</span></span>

  - <span data-ttu-id="40860-109">Добавление объекта **группы** или имя группы для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="40860-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="40860-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="40860-110">Remarks</span></span>

<span data-ttu-id="40860-111">Коллекцию **групп** [каталога](catalog-object-adox.md) предоставляет все учетные записи групп каталога.</span><span class="sxs-lookup"><span data-stu-id="40860-111">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts.</span></span> <span data-ttu-id="40860-112">Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="40860-112">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="40860-113">Если поставщик не поддерживает создание групп, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="40860-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <span data-ttu-id="40860-114">Перед добавлением объекта **группы** в коллекцию **групп** объекта **пользователя** , объект **группы** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекцию **групп** **каталога**.</span><span class="sxs-lookup"><span data-stu-id="40860-114">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


