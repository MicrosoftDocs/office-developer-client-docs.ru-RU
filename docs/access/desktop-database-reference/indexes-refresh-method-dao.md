---
title: Метод indexes. Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: ffe1bc79-5a56-2a70-c5ac-2f80b683adbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837325(v=office.15)
ms:contentKeyID: 48548973
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7e1b2a017342532f3eba1e14ce6097fea8ebffa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291485"
---
# <a name="indexesrefresh-method-dao"></a><span data-ttu-id="6f638-102">Метод indexes. Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f638-102">Indexes.Refresh method (DAO)</span></span>


<span data-ttu-id="6f638-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f638-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f638-104">Обновляет объекты в заданном коллетион в соответствии с текущей схемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="6f638-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f638-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f638-105">Syntax</span></span>

<span data-ttu-id="6f638-106">*Expression* . Обновление</span><span class="sxs-lookup"><span data-stu-id="6f638-106">*expression* .Refresh</span></span>

<span data-ttu-id="6f638-107">*Expression (выражение* ) Переменная, представляющая объект **индексов** .</span><span class="sxs-lookup"><span data-stu-id="6f638-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f638-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f638-108">Remarks</span></span>

<span data-ttu-id="6f638-109">Используйте метод **Refresh** в многопользовательской среде, в которой другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="6f638-109">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="6f638-110">Его также можно использовать для всех коллекций, на которые косвенно влияют изменения базы данных.</span><span class="sxs-lookup"><span data-stu-id="6f638-110">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="6f638-111">Например, если вы измените коллекцию **пользователей** , вам может потребоваться обновить коллекцию **Groups** перед использованием коллекции **Groups** .</span><span class="sxs-lookup"><span data-stu-id="6f638-111">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="6f638-112">Коллекция заполняется объектами, на которые она выполняется при первом запуске, и не автоматически отражает последующие изменения, внесенные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="6f638-112">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="6f638-113">Если, вероятно, другой пользователь изменил коллекцию, используйте метод Refresh в коллекции сразу же перед выполнением любой задачи в приложении, которая предполагает присутствие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="6f638-113">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="6f638-114">Это гарантирует, что коллекция будет как можно более актуальной.</span><span class="sxs-lookup"><span data-stu-id="6f638-114">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="6f638-115">С другой стороны, использование функции обновления может снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="6f638-115">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

