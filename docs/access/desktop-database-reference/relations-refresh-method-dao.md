---
title: Метод Relations.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: d71cecf2-da90-5f62-9e51-f994e660ad34
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835058(v=office.15)
ms:contentKeyID: 48547997
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9da7cdcead4f5143674f4b46f4a57d5c32dc62fa
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712052"
---
# <a name="relationsrefresh-method-dao"></a><span data-ttu-id="9e315-102">Метод Relations.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="9e315-102">Relations.Refresh method (DAO)</span></span>


<span data-ttu-id="9e315-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e315-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e315-104">Обновляет объекты в указанном включающий в соответствии с текущей схеме базы данных.</span><span class="sxs-lookup"><span data-stu-id="9e315-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e315-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e315-105">Syntax</span></span>

<span data-ttu-id="9e315-106">*выражение* . Обновление</span><span class="sxs-lookup"><span data-stu-id="9e315-106">*expression* .Refresh</span></span>

<span data-ttu-id="9e315-107">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="9e315-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e315-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e315-108">Remarks</span></span>

<span data-ttu-id="9e315-109">Используйте метод **Refresh** в многопользовательских средах, в которых другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="9e315-109">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="9e315-110">Кроме того, может потребоваться использовать на всех коллекций, которые косвенно затронуты изменениями в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9e315-110">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="9e315-111">Например при изменении коллекции **пользователей** может потребоваться обновить коллекцию **групп** перед использованием семейства сайтов **групп** .</span><span class="sxs-lookup"><span data-stu-id="9e315-111">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="9e315-112">Объекты в первый раз оно используется для ссылки и не отражает изменения, которые другие пользователи автоматически заполняется коллекцию.</span><span class="sxs-lookup"><span data-stu-id="9e315-112">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="9e315-113">Если это скорее всего, что другой пользователь был изменен коллекцию, используйте метод Refresh в семействе сайтов непосредственно перед выполнению любой из задач в приложения, которые предполагается наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="9e315-113">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="9e315-114">Это гарантирует, что коллекции с самым последним обновлением.</span><span class="sxs-lookup"><span data-stu-id="9e315-114">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="9e315-115">С другой стороны с помощью обновления без необходимости может снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="9e315-115">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

