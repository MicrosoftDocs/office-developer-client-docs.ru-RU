---
title: Удаление метода (ADOX коллекций)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 893890e43725d8c667ee5f72b396d3ec8947f395
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949371"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="59fd8-102">Удаление метода (ADOX коллекций)</span><span class="sxs-lookup"><span data-stu-id="59fd8-102">Delete method (ADOX Collections)</span></span>

<span data-ttu-id="59fd8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59fd8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="59fd8-104">Удаляет объект из коллекции.</span><span class="sxs-lookup"><span data-stu-id="59fd8-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="59fd8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59fd8-105">Syntax</span></span>

<span data-ttu-id="59fd8-106">*Семейства сайтов*. Удалите*имя*</span><span class="sxs-lookup"><span data-stu-id="59fd8-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="59fd8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="59fd8-107">Parameters</span></span>

|<span data-ttu-id="59fd8-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="59fd8-108">Parameter</span></span>|<span data-ttu-id="59fd8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="59fd8-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="59fd8-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="59fd8-110">*Name*</span></span> |<span data-ttu-id="59fd8-111">**Variant** , которое указывает имя или порядковый номер (индекс) объекта для удаления.</span><span class="sxs-lookup"><span data-stu-id="59fd8-111">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>|

## <a name="remarks"></a><span data-ttu-id="59fd8-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="59fd8-112">Remarks</span></span>

<span data-ttu-id="59fd8-113">Если *имя* не существует в коллекции, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="59fd8-113">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="59fd8-114">Для коллекций [таблиц](tables-collection-adox.md) и [пользователей](users-collection-adox.md) Если поставщик поддерживает удаление таблицы или пользователей, соответственно, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="59fd8-114">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively.</span></span> <span data-ttu-id="59fd8-115">Для коллекций, [представления](views-collection-adox.md) и [процедуры](procedures-collection-adox.md) **удалите** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="59fd8-115">For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

