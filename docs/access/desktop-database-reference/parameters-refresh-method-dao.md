---
title: Parameters.Refresh method (DAO)
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
# <a name="parametersrefresh-method-dao"></a><span data-ttu-id="e7973-102">Parameters.Refresh method (DAO)</span><span class="sxs-lookup"><span data-stu-id="e7973-102">Parameters.Refresh method (DAO)</span></span>


<span data-ttu-id="e7973-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7973-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7973-104">Обновляет объекты указанного коллегии, чтобы отразить текущую схему базы данных.</span><span class="sxs-lookup"><span data-stu-id="e7973-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7973-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7973-105">Syntax</span></span>

<span data-ttu-id="e7973-106">*выражения* . Обновление</span><span class="sxs-lookup"><span data-stu-id="e7973-106">*expression* .Refresh</span></span>

<span data-ttu-id="e7973-107">*выражение* Переменная, представляюная **объект Параметры.**</span><span class="sxs-lookup"><span data-stu-id="e7973-107">*expression* A variable that represents a **Parameters** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7973-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="e7973-108">Remarks</span></span>

<span data-ttu-id="e7973-109">Используйте метод **Refresh** в многоуровневой среде, в которой другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="e7973-109">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="e7973-110">Возможно, вам также потребуется использовать его в любых коллекциях, на которые косвенно влияют изменения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e7973-110">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="e7973-111">Например, если вы измените коллекцию **Пользователей,**  перед использованием коллекции Groups может потребоваться обновить коллекцию **Groups.**</span><span class="sxs-lookup"><span data-stu-id="e7973-111">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="e7973-112">Коллекция заполняется объектами при первой ссылке и не будет автоматически отражать последующие изменения, внесенные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="e7973-112">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="e7973-113">Если возможно, что другой пользователь изменил коллекцию, используйте метод Обновления в коллекции непосредственно перед тем, как выполнять любую задачу в приложении, предполагаемую наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e7973-113">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="e7973-114">Это гарантирует, что коллекция будет как можно более новой.</span><span class="sxs-lookup"><span data-stu-id="e7973-114">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="e7973-115">С другой стороны, использование Обновления может излишне замедлять производительность.</span><span class="sxs-lookup"><span data-stu-id="e7973-115">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

