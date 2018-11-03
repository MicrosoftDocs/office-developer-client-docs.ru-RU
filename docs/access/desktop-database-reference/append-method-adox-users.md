---
title: Метод Append (коллекция Users в ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e8b03bb74c5442eba3e1794d8067fa709f68af3d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931367"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="46bc6-102">Метод Append (коллекция Users в ADOX)</span><span class="sxs-lookup"><span data-stu-id="46bc6-102">Append method (ADOX Users)</span></span>


<span data-ttu-id="46bc6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46bc6-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="46bc6-104">Добавляет новый объект [пользователя](user-object-adox.md) в коллекции [пользователей](users-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="46bc6-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="46bc6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46bc6-105">Syntax</span></span>

<span data-ttu-id="46bc6-106">*Пользователи*. Добавление*пользователя*\[,*пароль*\]</span><span class="sxs-lookup"><span data-stu-id="46bc6-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="46bc6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="46bc6-107">Parameters</span></span>

  - <span data-ttu-id="46bc6-108">*user*</span><span class="sxs-lookup"><span data-stu-id="46bc6-108">*User*</span></span>

  - <span data-ttu-id="46bc6-109">Значение **типа Variant** , содержащее объект **пользователя** для добавления или имя пользователя для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="46bc6-109">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>

  - <span data-ttu-id="46bc6-110">*Password*</span><span class="sxs-lookup"><span data-stu-id="46bc6-110">*Password*</span></span>

  - <span data-ttu-id="46bc6-111">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="46bc6-111">Optional.</span></span> <span data-ttu-id="46bc6-112">**Строковое** значение, содержащее пароль для пользователя.</span><span class="sxs-lookup"><span data-stu-id="46bc6-112">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="46bc6-113">Параметр *Password* соответствует значению, указанному с помощью метода [Изменение пароля](changepassword-method-adox.md) объекта **пользователя** .</span><span class="sxs-lookup"><span data-stu-id="46bc6-113">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="46bc6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="46bc6-114">Remarks</span></span>

<span data-ttu-id="46bc6-115">Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="46bc6-115">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="46bc6-116">Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.</span><span class="sxs-lookup"><span data-stu-id="46bc6-116">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="46bc6-117">Если поставщик не поддерживает создание пользователей, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="46bc6-117">An error will occur if the provider does not support creating users.</span></span>


> [!NOTE]
> <span data-ttu-id="46bc6-118">Перед добавлением объекта **пользователя** в коллекцию **пользователей** объекта **группы** , объект **пользователя** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекции **пользователей** из **каталога**.</span><span class="sxs-lookup"><span data-stu-id="46bc6-118">Before appending a **User** object to the **Users** collection of a **Group** object, a **User** object with the same [Name](name-property-adox.md) as the one to be appended must already exist in the **Users** collection of the **Catalog**.</span></span>


