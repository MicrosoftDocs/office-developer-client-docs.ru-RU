---
title: Documents.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: 33405192-f23c-e2a2-feb6-9d641439cbc5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192321(v=office.15)
ms:contentKeyID: 48544100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a3070e5d07665465a5946ac8ace049576c14b04
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870186"
---
# <a name="documentsrefresh-method-dao"></a><span data-ttu-id="e08bb-102">Documents.Refresh Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="e08bb-102">Documents.Refresh Method (DAO)</span></span>


<span data-ttu-id="e08bb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e08bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e08bb-104">Обновляет объекты в указанном включающий в соответствии с текущей схеме базы данных.</span><span class="sxs-lookup"><span data-stu-id="e08bb-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="e08bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e08bb-105">Syntax</span></span>

<span data-ttu-id="e08bb-106">*выражение* . Обновление</span><span class="sxs-lookup"><span data-stu-id="e08bb-106">*expression* .Refresh</span></span>

<span data-ttu-id="e08bb-107">*выражение* Переменная, которая представляет собой объект- **документы** .</span><span class="sxs-lookup"><span data-stu-id="e08bb-107">*expression* A variable that represents a **Documents** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e08bb-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="e08bb-108">Remarks</span></span>

<span data-ttu-id="e08bb-109">Используйте метод **Refresh** в многопользовательских средах, в которых другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="e08bb-109">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="e08bb-110">Кроме того, может потребоваться использовать на всех коллекций, которые косвенно затронуты изменениями в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e08bb-110">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="e08bb-111">Например при изменении коллекции **пользователей** может потребоваться обновить коллекцию **групп** перед использованием семейства сайтов **групп** .</span><span class="sxs-lookup"><span data-stu-id="e08bb-111">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="e08bb-112">Объекты в первый раз оно используется для ссылки и не отражает изменения, которые другие пользователи автоматически заполняется коллекцию.</span><span class="sxs-lookup"><span data-stu-id="e08bb-112">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="e08bb-113">Если это скорее всего, что другой пользователь был изменен коллекцию, используйте метод Refresh в семействе сайтов непосредственно перед выполнению любой из задач в приложения, которые предполагается наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e08bb-113">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="e08bb-114">Это гарантирует, что коллекции с самым последним обновлением.</span><span class="sxs-lookup"><span data-stu-id="e08bb-114">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="e08bb-115">С другой стороны с помощью обновления без необходимости может снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="e08bb-115">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

