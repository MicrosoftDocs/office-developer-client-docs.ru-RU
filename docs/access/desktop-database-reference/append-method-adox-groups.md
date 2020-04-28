---
title: Метод Append (коллекция Groups в ADOX)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0e7731777e3d82e3746c3886bdbddb3e43db66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297104"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="3ef42-102">Метод Append (коллекция Groups в ADOX)</span><span class="sxs-lookup"><span data-stu-id="3ef42-102">Append method (ADOX Groups)</span></span>

<span data-ttu-id="3ef42-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ef42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ef42-104">Добавляет новый объект [Group](group-object-adox.md) в коллекцию [Groups](groups-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="3ef42-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ef42-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ef42-105">Syntax</span></span>

<span data-ttu-id="3ef42-106">*Группы*. Добавление*группы*</span><span class="sxs-lookup"><span data-stu-id="3ef42-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="3ef42-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ef42-107">Parameters</span></span>

|<span data-ttu-id="3ef42-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="3ef42-108">Parameter</span></span>|<span data-ttu-id="3ef42-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3ef42-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3ef42-110">*Group*</span><span class="sxs-lookup"><span data-stu-id="3ef42-110">*Group*</span></span> |<span data-ttu-id="3ef42-111">Объект **Group** , который требуется добавить, или имя группы, которую требуется создать и добавить.</span><span class="sxs-lookup"><span data-stu-id="3ef42-111">The **Group** object to append or the name of the group to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3ef42-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ef42-112">Remarks</span></span>

<span data-ttu-id="3ef42-113">Коллекция **Groups** [каталога](catalog-object-adox.md) представляет все учетные записи групп в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3ef42-113">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts.</span></span> <span data-ttu-id="3ef42-114">Коллекция **Groups** для [пользователя](user-object-adox.md) представляет только группу, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="3ef42-114">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="3ef42-115">Если поставщик не поддерживает создание групп, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3ef42-115">An error will occur if the provider does not support creating groups.</span></span>

> [!NOTE]
> <span data-ttu-id="3ef42-116">Перед добавлением объекта **Group** в коллекцию **Groups** объекта **User** объект **Group** с тем же [именем](name-property-adox.md) , что и у добавляемого объекта, должен уже существовать в коллекции **Groups** **каталога**.</span><span class="sxs-lookup"><span data-stu-id="3ef42-116">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


