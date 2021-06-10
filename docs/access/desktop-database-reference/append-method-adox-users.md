---
title: Метод Append (коллекция Users в ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d05cf352515d8fe4faa868088c9ba9cc8a024145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297069"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="1688b-102">Метод Append (коллекция Users в ADOX)</span><span class="sxs-lookup"><span data-stu-id="1688b-102">Append method (ADOX Users)</span></span>

<span data-ttu-id="1688b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1688b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1688b-104">Добавляет новый [объект User](user-object-adox.md) в коллекцию [Пользователей.](users-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="1688b-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1688b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1688b-105">Syntax</span></span>

<span data-ttu-id="1688b-106">*Пользователи*. Пользователь *приложения* \[ ,*пароль*\]</span><span class="sxs-lookup"><span data-stu-id="1688b-106">*Users*.Append *User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="1688b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1688b-107">Parameters</span></span>

|<span data-ttu-id="1688b-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="1688b-108">Parameter</span></span>|<span data-ttu-id="1688b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1688b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1688b-110">*Пользователь*</span><span class="sxs-lookup"><span data-stu-id="1688b-110">*User*</span></span> |<span data-ttu-id="1688b-111">Значение **Variant,** содержаное объект **Пользователя** для приложения или имя пользователя для создания и приложения.</span><span class="sxs-lookup"><span data-stu-id="1688b-111">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>|
|<span data-ttu-id="1688b-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="1688b-112">*Password*</span></span> |<span data-ttu-id="1688b-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="1688b-113">Optional.</span></span> <span data-ttu-id="1688b-114">Значение **String,** содержа которое содержит пароль для пользователя.</span><span class="sxs-lookup"><span data-stu-id="1688b-114">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="1688b-115">Параметр *Password* соответствует значению, указанному методом [ChangePassword](changepassword-method-adox.md) объекта **Пользователя.**</span><span class="sxs-lookup"><span data-stu-id="1688b-115">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1688b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="1688b-116">Remarks</span></span>

<span data-ttu-id="1688b-117">Коллекция **"Пользователи** [каталога"](catalog-object-adox.md) представляет всех пользователей каталога.</span><span class="sxs-lookup"><span data-stu-id="1688b-117">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="1688b-118">Коллекция **Пользователей** для [группы представляет](group-object-adox.md) только пользователей, которые имеют членство в определенной группе.</span><span class="sxs-lookup"><span data-stu-id="1688b-118">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="1688b-119">Ошибка произойдет, если поставщик не поддерживает создание пользователей.</span><span class="sxs-lookup"><span data-stu-id="1688b-119">An error will occur if the provider does not support creating users.</span></span>

> [!NOTE]
> <span data-ttu-id="1688b-120">Прежде чем примковать  объект Пользователя к коллекции  Пользователей объекта **Group,** объект User с тем же именем, что и объект, который должен быть придан, уже должен существовать в коллекции **Пользователей**  **каталога.** [](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="1688b-120">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


