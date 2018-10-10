---
title: Delete Method (ADOX Collections)
TOCTitle: Delete Method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea02f02270649783873f1f086bb9f39b804034a2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482697"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="7d879-102">Delete Method (ADOX Collections)</span><span class="sxs-lookup"><span data-stu-id="7d879-102">Delete Method (ADOX Collections)</span></span>


<span data-ttu-id="7d879-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d879-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="7d879-104">Удаляет объект из коллекции.</span><span class="sxs-lookup"><span data-stu-id="7d879-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d879-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d879-105">Syntax</span></span>

<span data-ttu-id="7d879-106">*Семейства сайтов*. Удалите*имя*</span><span class="sxs-lookup"><span data-stu-id="7d879-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="7d879-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d879-107">Parameters</span></span>

  - <span data-ttu-id="7d879-108">*Имя*</span><span class="sxs-lookup"><span data-stu-id="7d879-108">*Name*</span></span>

  - <span data-ttu-id="7d879-109">**Variant** , которое указывает имя или порядковый номер (индекс) объекта для удаления.</span><span class="sxs-lookup"><span data-stu-id="7d879-109">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d879-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="7d879-110">Remarks</span></span>

<span data-ttu-id="7d879-111">Если *имя* не существует в коллекции, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7d879-111">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="7d879-112">Для коллекций [таблиц](tables-collection-adox.md) и [пользователей](users-collection-adox.md) Если поставщик поддерживает удаление таблицы или пользователей, соответственно, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7d879-112">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively.</span></span> <span data-ttu-id="7d879-113">Для коллекций, [представления](views-collection-adox.md) и [процедуры](procedures-collection-adox.md) **удалите** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="7d879-113">For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

