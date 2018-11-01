---
title: Errors.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: dc352c5f-09d0-bfb3-b24a-4c3454dbf5aa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835359(v=office.15)
ms:contentKeyID: 48548127
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 55a87b30a30342a586cc3a5284d51035be5b910f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869752"
---
# <a name="errorsrefresh-method-dao"></a><span data-ttu-id="4164f-102">Errors.Refresh Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="4164f-102">Errors.Refresh Method (DAO)</span></span>


<span data-ttu-id="4164f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4164f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4164f-104">Обновляет объекты в указанном включающий в соответствии с текущей схеме базы данных.</span><span class="sxs-lookup"><span data-stu-id="4164f-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="4164f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4164f-105">Syntax</span></span>

<span data-ttu-id="4164f-106">*выражение* . Обновление</span><span class="sxs-lookup"><span data-stu-id="4164f-106">*expression* .Refresh</span></span>

<span data-ttu-id="4164f-107">*выражение* Переменная, которая представляет объект **ошибки** .</span><span class="sxs-lookup"><span data-stu-id="4164f-107">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4164f-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="4164f-108">Remarks</span></span>

<span data-ttu-id="4164f-109">Используйте метод **Refresh** в многопользовательских средах, в которых другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="4164f-109">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="4164f-110">Кроме того, может потребоваться использовать на всех коллекций, которые косвенно затронуты изменениями в базе данных.</span><span class="sxs-lookup"><span data-stu-id="4164f-110">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="4164f-111">Например при изменении коллекции **пользователей** может потребоваться обновить коллекцию **групп** перед использованием семейства сайтов **групп** .</span><span class="sxs-lookup"><span data-stu-id="4164f-111">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="4164f-112">Объекты в первый раз оно используется для ссылки и не отражает изменения, которые другие пользователи автоматически заполняется коллекцию.</span><span class="sxs-lookup"><span data-stu-id="4164f-112">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="4164f-113">Если это скорее всего, что другой пользователь был изменен коллекцию, используйте метод Refresh в семействе сайтов непосредственно перед выполнению любой из задач в приложения, которые предполагается наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="4164f-113">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="4164f-114">Это гарантирует, что коллекции с самым последним обновлением.</span><span class="sxs-lookup"><span data-stu-id="4164f-114">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="4164f-115">С другой стороны с помощью обновления без необходимости может снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="4164f-115">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

