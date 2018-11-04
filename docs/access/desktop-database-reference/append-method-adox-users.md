---
title: Метод Append (коллекция Users в ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf855fc6e829ebfbe3809925bf1ab8ca337d3f96
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949413"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="49aeb-102">Метод Append (коллекция Users в ADOX)</span><span class="sxs-lookup"><span data-stu-id="49aeb-102">Append method (ADOX Users)</span></span>

<span data-ttu-id="49aeb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49aeb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49aeb-104">Добавляет новый объект [пользователя](user-object-adox.md) в коллекции [пользователей](users-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="49aeb-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="49aeb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49aeb-105">Syntax</span></span>

<span data-ttu-id="49aeb-106">*Пользователи*. Добавление*пользователя*\[,*пароль*\]</span><span class="sxs-lookup"><span data-stu-id="49aeb-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="49aeb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="49aeb-107">Parameters</span></span>

|<span data-ttu-id="49aeb-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="49aeb-108">Parameter</span></span>|<span data-ttu-id="49aeb-109">Описание</span><span class="sxs-lookup"><span data-stu-id="49aeb-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="49aeb-110">*user*</span><span class="sxs-lookup"><span data-stu-id="49aeb-110">*User*</span></span> |<span data-ttu-id="49aeb-111">Значение **типа Variant** , содержащее объект **пользователя** для добавления или имя пользователя для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="49aeb-111">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>|
|<span data-ttu-id="49aeb-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="49aeb-112">*Password*</span></span> |<span data-ttu-id="49aeb-113">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="49aeb-113">Optional.</span></span> <span data-ttu-id="49aeb-114">**Строковое** значение, содержащее пароль для пользователя.</span><span class="sxs-lookup"><span data-stu-id="49aeb-114">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="49aeb-115">Параметр *Password* соответствует значению, указанному с помощью метода [Изменение пароля](changepassword-method-adox.md) объекта **пользователя** .</span><span class="sxs-lookup"><span data-stu-id="49aeb-115">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="49aeb-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="49aeb-116">Remarks</span></span>

<span data-ttu-id="49aeb-117">Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="49aeb-117">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="49aeb-118">Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.</span><span class="sxs-lookup"><span data-stu-id="49aeb-118">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="49aeb-119">Если поставщик не поддерживает создание пользователей, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="49aeb-119">An error will occur if the provider does not support creating users.</span></span>

> [!NOTE]
> <span data-ttu-id="49aeb-120">Перед добавлением объекта **пользователя** в коллекцию **пользователей** объекта **группы** , объект **пользователя** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекции **пользователей** из **каталога**.</span><span class="sxs-lookup"><span data-stu-id="49aeb-120">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


