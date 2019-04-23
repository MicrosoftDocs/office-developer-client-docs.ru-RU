---
title: Метод Parameters. Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: 47db1602-e223-985d-881c-b73e2d26acb7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193228(v=office.15)
ms:contentKeyID: 48544607
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29374baf16ec6c296f869b6bbf17bfb153d21bb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287778"
---
# <a name="parametersrefresh-method-dao"></a><span data-ttu-id="5cb10-102">Метод Parameters. Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="5cb10-102">Parameters.Refresh method (DAO)</span></span>


<span data-ttu-id="5cb10-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cb10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5cb10-104">Обновляет объекты в заданном коллетион в соответствии с текущей схемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="5cb10-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cb10-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cb10-105">Syntax</span></span>

<span data-ttu-id="5cb10-106">*Expression* . Обновление</span><span class="sxs-lookup"><span data-stu-id="5cb10-106">*expression* .Refresh</span></span>

<span data-ttu-id="5cb10-107">*Expression (выражение* ) Переменная, представляющая объект **Parameters** .</span><span class="sxs-lookup"><span data-stu-id="5cb10-107">*expression* A variable that represents a **Parameters** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cb10-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="5cb10-108">Remarks</span></span>

<span data-ttu-id="5cb10-109">Используйте метод **Refresh** в многопользовательской среде, в которой другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="5cb10-109">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="5cb10-110">Его также можно использовать для всех коллекций, на которые косвенно влияют изменения базы данных.</span><span class="sxs-lookup"><span data-stu-id="5cb10-110">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="5cb10-111">Например, если вы измените коллекцию **пользователей** , вам может потребоваться обновить коллекцию **Groups** перед использованием коллекции **Groups** .</span><span class="sxs-lookup"><span data-stu-id="5cb10-111">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="5cb10-112">Коллекция заполняется объектами, на которые она выполняется при первом запуске, и не автоматически отражает последующие изменения, внесенные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="5cb10-112">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="5cb10-113">Если, вероятно, другой пользователь изменил коллекцию, используйте метод Refresh в коллекции сразу же перед выполнением любой задачи в приложении, которая предполагает присутствие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="5cb10-113">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="5cb10-114">Это гарантирует, что коллекция будет как можно более актуальной.</span><span class="sxs-lookup"><span data-stu-id="5cb10-114">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="5cb10-115">С другой стороны, использование функции обновления может снизить производительность.</span><span class="sxs-lookup"><span data-stu-id="5cb10-115">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

