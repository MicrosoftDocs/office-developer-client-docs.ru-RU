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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707600"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="d896f-102">Метод Append (коллекция Users в ADOX)</span><span class="sxs-lookup"><span data-stu-id="d896f-102">Append method (ADOX Users)</span></span>

<span data-ttu-id="d896f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d896f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d896f-104">Добавляет новый объект [пользователя](user-object-adox.md) в коллекции [пользователей](users-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="d896f-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d896f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d896f-105">Syntax</span></span>

<span data-ttu-id="d896f-106">*Пользователи*. Добавление*пользователя*\[,*пароль*\]</span><span class="sxs-lookup"><span data-stu-id="d896f-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="d896f-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d896f-107">Parameters</span></span>

|<span data-ttu-id="d896f-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d896f-108">Parameter</span></span>|<span data-ttu-id="d896f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d896f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d896f-110">*user*</span><span class="sxs-lookup"><span data-stu-id="d896f-110">*User*</span></span> |<span data-ttu-id="d896f-111">Значение **типа Variant** , содержащее объект **пользователя** для добавления или имя пользователя для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="d896f-111">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>|
|<span data-ttu-id="d896f-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="d896f-112">*Password*</span></span> |<span data-ttu-id="d896f-113">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="d896f-113">Optional.</span></span> <span data-ttu-id="d896f-114">**Строковое** значение, содержащее пароль для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d896f-114">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="d896f-115">Параметр *Password* соответствует значению, указанному с помощью метода [Изменение пароля](changepassword-method-adox.md) объекта **пользователя** .</span><span class="sxs-lookup"><span data-stu-id="d896f-115">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d896f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d896f-116">Remarks</span></span>

<span data-ttu-id="d896f-117">Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="d896f-117">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="d896f-118">Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.</span><span class="sxs-lookup"><span data-stu-id="d896f-118">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="d896f-119">Если поставщик не поддерживает создание пользователей, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="d896f-119">An error will occur if the provider does not support creating users.</span></span>

> [!NOTE]
> <span data-ttu-id="d896f-120">Перед добавлением объекта **пользователя** в коллекцию **пользователей** объекта **группы** , объект **пользователя** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекции **пользователей** из **каталога**.</span><span class="sxs-lookup"><span data-stu-id="d896f-120">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


