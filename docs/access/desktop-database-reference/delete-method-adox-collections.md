---
title: Метод Delete (коллекции ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294080"
---
# <a name="delete-method-adox-collections"></a><span data-ttu-id="17851-102">Метод Delete (коллекции ADOX)</span><span class="sxs-lookup"><span data-stu-id="17851-102">Delete method (ADOX Collections)</span></span>

<span data-ttu-id="17851-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17851-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17851-104">Удаляет объект из коллекции.</span><span class="sxs-lookup"><span data-stu-id="17851-104">Removes an object from a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="17851-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17851-105">Syntax</span></span>

<span data-ttu-id="17851-106">*Коллекция*. Удаление*имени*</span><span class="sxs-lookup"><span data-stu-id="17851-106">*Collection*.Delete*Name*</span></span>

## <a name="parameters"></a><span data-ttu-id="17851-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="17851-107">Parameters</span></span>

|<span data-ttu-id="17851-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="17851-108">Parameter</span></span>|<span data-ttu-id="17851-109">Описание</span><span class="sxs-lookup"><span data-stu-id="17851-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="17851-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="17851-110">*Name*</span></span> |<span data-ttu-id="17851-111">**Значение Variant** , задающее имя или порядковый номер объекта, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="17851-111">A **Variant** that specifies the name or ordinal position (index) of the object to delete.</span></span>|

## <a name="remarks"></a><span data-ttu-id="17851-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="17851-112">Remarks</span></span>

<span data-ttu-id="17851-113">Если *имя* не существует в коллекции, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="17851-113">An error will occur if the *Name* does not exist in the collection.</span></span>

<span data-ttu-id="17851-114">Для коллекций [таблиц](tables-collection-adox.md) и [пользователей](users-collection-adox.md) возникает ошибка, если поставщик не поддерживает удаление таблиц или пользователей соответственно.</span><span class="sxs-lookup"><span data-stu-id="17851-114">For [Tables](tables-collection-adox.md) and [Users](users-collection-adox.md) collections, an error will occur if the provider does not support deleting tables or users, respectively.</span></span> <span data-ttu-id="17851-115">Для коллекций [процедур](procedures-collection-adox.md) и [представлений](views-collection-adox.md) **Удаление** завершится с ошибками, если поставщик не поддерживает хранимые команды.</span><span class="sxs-lookup"><span data-stu-id="17851-115">For [Procedures](procedures-collection-adox.md) and [Views](views-collection-adox.md) collections, **Delete** will fail if the provider does not support persisting commands.</span></span>

