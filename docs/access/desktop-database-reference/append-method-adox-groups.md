---
title: Append Method (ADOX Groups)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c602896a629881d06a3f3cf80326e02340186e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482816"
---
# <a name="append-method-adox-groups"></a><span data-ttu-id="ede6d-102">Append Method (ADOX Groups)</span><span class="sxs-lookup"><span data-stu-id="ede6d-102">Append Method (ADOX Groups)</span></span>


<span data-ttu-id="ede6d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ede6d-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="ede6d-104">Добавляет новый объект [групповой](group-object-adox.md) в коллекцию [групп](groups-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="ede6d-104">Adds a new [Group](group-object-adox.md) object to the [Groups](groups-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede6d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ede6d-105">Syntax</span></span>

<span data-ttu-id="ede6d-106">*Группы*. Добавление*группы*</span><span class="sxs-lookup"><span data-stu-id="ede6d-106">*Groups*.Append*Group*</span></span>

## <a name="parameters"></a><span data-ttu-id="ede6d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ede6d-107">Parameters</span></span>

  - <span data-ttu-id="ede6d-108">*group*</span><span class="sxs-lookup"><span data-stu-id="ede6d-108">*Group*</span></span>

  - <span data-ttu-id="ede6d-109">Добавление объекта **группы** или имя группы для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="ede6d-109">The **Group** object to append or the name of the group to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="ede6d-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="ede6d-110">Remarks</span></span>

<span data-ttu-id="ede6d-111">Коллекцию **групп** [каталога](catalog-object-adox.md) предоставляет все учетные записи групп каталога.</span><span class="sxs-lookup"><span data-stu-id="ede6d-111">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts.</span></span> <span data-ttu-id="ede6d-112">Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.</span><span class="sxs-lookup"><span data-stu-id="ede6d-112">The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="ede6d-113">Если поставщик не поддерживает создание групп, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="ede6d-113">An error will occur if the provider does not support creating groups.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ede6d-114">Перед добавлением объекта <STRONG>группы</STRONG> в коллекцию <STRONG>групп</STRONG> объекта <STRONG>пользователя</STRONG> , объект <STRONG>группы</STRONG> с тем же <A href="name-property-adox.md">именем</A> , который будет добавляться должны уже существовать в коллекцию <STRONG>групп</STRONG> <STRONG>каталога</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ede6d-114">Before appending a <STRONG>Group</STRONG> object to the <STRONG>Groups</STRONG> collection of a <STRONG>User</STRONG> object, a <STRONG>Group</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Groups</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


