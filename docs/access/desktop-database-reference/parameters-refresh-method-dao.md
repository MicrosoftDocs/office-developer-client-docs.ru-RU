---
title: Метод Parameters.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: 47db1602-e223-985d-881c-b73e2d26acb7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193228(v=office.15)
ms:contentKeyID: 48544607
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29374baf16ec6c296f869b6bbf17bfb153d21bb3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704058"
---
# <a name="parametersrefresh-method-dao"></a><span data-ttu-id="b329a-102">Метод Parameters.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="b329a-102">Parameters.Refresh method (DAO)</span></span>


<span data-ttu-id="b329a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b329a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b329a-104">Обновляет объекты в указанном включающий в соответствии с текущей схеме базы данных.</span><span class="sxs-lookup"><span data-stu-id="b329a-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="b329a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b329a-105">Syntax</span></span>

<span data-ttu-id="b329a-106">*выражение* . Обновление</span><span class="sxs-lookup"><span data-stu-id="b329a-106">*expression* .Refresh</span></span>

<span data-ttu-id="b329a-107">*выражение* Переменная, которая представляет собой объект- **Параметры** .</span><span class="sxs-lookup"><span data-stu-id="b329a-107">*expression* A variable that represents a **Parameters** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b329a-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="b329a-108">Remarks</span></span>

<span data-ttu-id="b329a-109">Используйте метод **Refresh** в многопользовательских средах, в которых другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="b329a-109">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="b329a-110">Кроме того, может потребоваться использовать на всех коллекций, которые косвенно затронуты изменениями в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b329a-110">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="b329a-111">Например при изменении коллекции **пользователей** может потребоваться обновить коллекцию **групп** перед использованием семейства сайтов **групп** .</span><span class="sxs-lookup"><span data-stu-id="b329a-111">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="b329a-112">Объекты в первый раз оно используется для ссылки и не отражает изменения, которые другие пользователи автоматически заполняется коллекцию.</span><span class="sxs-lookup"><span data-stu-id="b329a-112">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="b329a-113">Если это скорее всего, что другой пользователь был изменен коллекцию, используйте метод Refresh в семействе сайтов непосредственно перед выполнению любой из задач в приложения, которые предполагается наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b329a-113">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="b329a-114">Это гарантирует, что коллекции с самым последним обновлением.</span><span class="sxs-lookup"><span data-stu-id="b329a-114">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="b329a-115">С другой стороны с помощью обновления без необходимости может снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="b329a-115">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

