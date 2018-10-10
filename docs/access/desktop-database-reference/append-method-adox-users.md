---
title: Append Method (ADOX Users)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8bce151e800b58e9c99c6dd6591114c53208a5c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480569"
---
# <a name="append-method-adox-users"></a><span data-ttu-id="035f9-102">Append Method (ADOX Users)</span><span class="sxs-lookup"><span data-stu-id="035f9-102">Append Method (ADOX Users)</span></span>


<span data-ttu-id="035f9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="035f9-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="035f9-104">Добавляет новый объект [пользователя](user-object-adox.md) в коллекции [пользователей](users-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="035f9-104">Adds a new [User](user-object-adox.md) object to the [Users](users-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="035f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="035f9-105">Syntax</span></span>

<span data-ttu-id="035f9-106">*Пользователи*. Добавление*пользователя*\[,*пароль*\]</span><span class="sxs-lookup"><span data-stu-id="035f9-106">*Users*.Append*User*\[,*Password*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="035f9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="035f9-107">Parameters</span></span>

  - <span data-ttu-id="035f9-108">*user*</span><span class="sxs-lookup"><span data-stu-id="035f9-108">*User*</span></span>

  - <span data-ttu-id="035f9-109">Значение **типа Variant** , содержащее объект **пользователя** для добавления или имя пользователя для создания и добавления.</span><span class="sxs-lookup"><span data-stu-id="035f9-109">A **Variant** value that contains the **User** object to append or the name of the user to create and append.</span></span>

  - <span data-ttu-id="035f9-110">*Password*</span><span class="sxs-lookup"><span data-stu-id="035f9-110">*Password*</span></span>

  - <span data-ttu-id="035f9-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="035f9-111">Optional.</span></span> <span data-ttu-id="035f9-112">**Строковое** значение, содержащее пароль для пользователя.</span><span class="sxs-lookup"><span data-stu-id="035f9-112">A **String** value that contains the password for the user.</span></span> <span data-ttu-id="035f9-113">Параметр *Password* соответствует значению, указанному с помощью метода [Изменение пароля](changepassword-method-adox.md) объекта **пользователя** .</span><span class="sxs-lookup"><span data-stu-id="035f9-113">The *Password* parameter corresponds to the value specified by the [ChangePassword](changepassword-method-adox.md) method of a **User** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="035f9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="035f9-114">Remarks</span></span>

<span data-ttu-id="035f9-115">Коллекция **пользователей** из [каталога](catalog-object-adox.md) представляет каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="035f9-115">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users.</span></span> <span data-ttu-id="035f9-116">Коллекция **пользователей** для [группы](group-object-adox.md) представляет пользователей, которые состоят в конкретную группу.</span><span class="sxs-lookup"><span data-stu-id="035f9-116">The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="035f9-117">Если поставщик не поддерживает создание пользователей, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="035f9-117">An error will occur if the provider does not support creating users.</span></span>


> [!NOTE]
> <P><span data-ttu-id="035f9-118">Перед добавлением объекта <STRONG>пользователя</STRONG> в коллекцию <STRONG>пользователей</STRONG> объекта <STRONG>группы</STRONG> , объект <STRONG>пользователя</STRONG> с тем же <A href="name-property-adox.md">именем</A> , который будет добавляться должны уже существовать в коллекции <STRONG>пользователей</STRONG> из <STRONG>каталога</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="035f9-118">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


