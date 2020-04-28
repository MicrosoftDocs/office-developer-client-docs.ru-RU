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
# <a name="append-method-adox-users"></a><span data-ttu-id="73ccf-102">Метод Append (коллекция Users в ADOX)</span><span class="sxs-lookup"><span data-stu-id="73ccf-102">Append method (ADOX Users)</span></span>

<span data-ttu-id="73ccf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73ccf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73ccf-104">Добавляет новый объект [User](user-object-adox.md) в коллекцию [Users](users-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="73ccf-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ccf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73ccf-105">Syntax</span></span>

<span data-ttu-id="73ccf-106">*Пользователи*. Добавление*пользователя*\[,*пароль*\]</span><span class="sxs-lookup"><span data-stu-id="73ccf-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="73ccf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="73ccf-107">Parameters</span></span>

|<span data-ttu-id="73ccf-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="73ccf-108">Parameter</span></span>|<span data-ttu-id="73ccf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="73ccf-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="73ccf-110">*User*</span><span class="sxs-lookup"><span data-stu-id="73ccf-110">*User*</span></span> |<span data-ttu-id="73ccf-111">Значение **Variant** , содержащее объект **пользователя** для добавления или имя пользователя, для которого создается и добавляется.</span><span class="sxs-lookup"><span data-stu-id="73ccf-111">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>|
|<span data-ttu-id="73ccf-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="73ccf-112">*Password*</span></span> |<span data-ttu-id="73ccf-113">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="73ccf-113">Optional.</span></span> <span data-ttu-id="73ccf-114">**Строковое** значение, содержащее пароль для пользователя.</span><span class="sxs-lookup"><span data-stu-id="73ccf-114">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="73ccf-115">Параметр *Password* соответствует значению, указанному в методе [ChangePassword](changepassword-method-adox.md) объекта **пользователя** .</span><span class="sxs-lookup"><span data-stu-id="73ccf-115">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="73ccf-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="73ccf-116">Remarks</span></span>

<span data-ttu-id="73ccf-117">Коллекция **Users каталога Users** содержит все пользователи каталога. [Catalog](catalog-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="73ccf-117">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="73ccf-118">Коллекция **Users** для [группы](group-object-adox.md) представляет только тех пользователей, у которых есть членство в определенной группе.</span><span class="sxs-lookup"><span data-stu-id="73ccf-118">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="73ccf-119">Если поставщик не поддерживает создание пользователей, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="73ccf-119">An error will occur if the provider does not support creating users.</span></span>

> [!NOTE]
> <span data-ttu-id="73ccf-120">Перед добавлением объекта **User** в коллекцию **Users** объекта **Group** объект **пользователя** с тем же [именем](name-property-adox.md) , что и у добавляемого объекта, должен уже существовать в коллекции **Users** **каталога**.</span><span class="sxs-lookup"><span data-stu-id="73ccf-120">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


