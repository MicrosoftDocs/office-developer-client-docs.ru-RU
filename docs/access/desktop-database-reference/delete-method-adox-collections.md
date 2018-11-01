---
title: Удаление метода (ADOX коллекций)
TOCTitle: Delete Method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bfb9e12f32da56aecd9338e51d6e4656714b6c1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871334"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="84b30-102">Удаление метода (ADOX коллекций)</span><span class="sxs-lookup"><span data-stu-id="84b30-102">Delete Method (ADOX Collections)</span></span>


<span data-ttu-id="84b30-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84b30-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="84b30-104">Удаляет объект из коллекции.</span><span class="sxs-lookup"><span data-stu-id="84b30-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="84b30-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84b30-105">Syntax</span></span>

<span data-ttu-id="84b30-106">*Семейства сайтов*. Удалите*имя*</span><span class="sxs-lookup"><span data-stu-id="84b30-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="84b30-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="84b30-107">Parameters</span></span>

  - <span data-ttu-id="84b30-108">*Имя*</span><span class="sxs-lookup"><span data-stu-id="84b30-108">*Name*</span></span>

  - <span data-ttu-id="84b30-109">**Variant** , которое указывает имя или порядковый номер (индекс) объекта для удаления.</span><span class="sxs-lookup"><span data-stu-id="84b30-109">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>

## <a name="remarks"></a><span data-ttu-id="84b30-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="84b30-110">Remarks</span></span>

<span data-ttu-id="84b30-111">Если *имя* не существует в коллекции, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="84b30-111">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="84b30-112">Для коллекций [таблиц](tables-collection-adox.md) и [пользователей](users-collection-adox.md) Если поставщик поддерживает удаление таблицы или пользователей, соответственно, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="84b30-112">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively.</span></span> <span data-ttu-id="84b30-113">Для коллекций, [представления](views-collection-adox.md) и [процедуры](procedures-collection-adox.md) **удалите** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="84b30-113">For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

