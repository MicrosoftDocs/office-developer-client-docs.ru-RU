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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709028"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="df07e-102">Метод Append (коллекция Groups в ADOX)</span><span class="sxs-lookup"><span data-stu-id="df07e-102">Append method (ADOX Groups)</span></span>

<span data-ttu-id="df07e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df07e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df07e-104">Добавляет новый объект [групповой](group-object-adox.md) в коллекцию [групп](groups-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="df07e-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="df07e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df07e-105">Syntax</span></span>

<span data-ttu-id="df07e-106">*Группы*. Добавление*группы*</span><span class="sxs-lookup"><span data-stu-id="df07e-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="df07e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="df07e-107">Parameters</span></span>

|<span data-ttu-id="df07e-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="df07e-108">Parameter</span></span>|<span data-ttu-id="df07e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="df07e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="df07e-110">*Group*</span><span class="sxs-lookup"><span data-stu-id="df07e-110">*Group*</span></span> |<span data-ttu-id="df07e-111">Добавление объекта **группы** или имя группы для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="df07e-111">The **Group** object to append or the name of the group to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="df07e-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="df07e-112">Remarks</span></span>

<span data-ttu-id="df07e-113">Коллекцию **групп** [каталога](catalog-object-adox.md) предоставляет все учетные записи групп каталога.</span><span class="sxs-lookup"><span data-stu-id="df07e-113">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts.</span></span> <span data-ttu-id="df07e-114">Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="df07e-114">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="df07e-115">Если поставщик не поддерживает создание групп, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="df07e-115">An error will occur if the provider does not support creating groups.</span></span>

> [!NOTE]
> <span data-ttu-id="df07e-116">Перед добавлением объекта **группы** в коллекцию **групп** объекта **пользователя** , объект **группы** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекцию **групп** **каталога**.</span><span class="sxs-lookup"><span data-stu-id="df07e-116">Before appending a **Group** object to the **Groups** collection of a **User** object, a **Group** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Groups** collection of the **Catalog**.</span></span>


