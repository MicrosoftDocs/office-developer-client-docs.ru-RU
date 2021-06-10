---
title: Метод Properties.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: 71ba18fb-55a5-6a5f-3631-1c81c20f3369
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195805(v=office.15)
ms:contentKeyID: 48545593
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9d6b248bc4b8d9c1a9e01db0231bf58b16c36dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301199"
---
# <a name="propertiesrefresh-method-dao"></a><span data-ttu-id="e547d-102">Метод Properties.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="e547d-102">Properties.Refresh method (DAO)</span></span>


<span data-ttu-id="e547d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e547d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e547d-104">Обновляет объекты указанного коллегии, чтобы отразить текущую схему базы данных.</span><span class="sxs-lookup"><span data-stu-id="e547d-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="e547d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e547d-105">Syntax</span></span>

<span data-ttu-id="e547d-106">*выражения* . Обновление</span><span class="sxs-lookup"><span data-stu-id="e547d-106">*expression* .Refresh</span></span>

<span data-ttu-id="e547d-107">*выражение* Переменная, представляюная объект **Properties.**</span><span class="sxs-lookup"><span data-stu-id="e547d-107">*expression* A variable that represents a **Properties** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e547d-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="e547d-108">Remarks</span></span>

<span data-ttu-id="e547d-109">Используйте метод **Refresh** в многоуровневой среде, в которой другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="e547d-109">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="e547d-110">Возможно, вам также потребуется использовать его в любых коллекциях, на которые косвенно влияют изменения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e547d-110">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="e547d-111">Например, если вы измените коллекцию **Пользователей,**  перед использованием коллекции Groups может потребоваться обновить коллекцию **Groups.**</span><span class="sxs-lookup"><span data-stu-id="e547d-111">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="e547d-112">Коллекция заполняется объектами при первой ссылке и не будет автоматически отражать последующие изменения, внесенные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="e547d-112">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="e547d-113">Если возможно, что другой пользователь изменил коллекцию, используйте метод Обновления в коллекции непосредственно перед тем, как выполнять любую задачу в приложении, предполагаемую наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e547d-113">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="e547d-114">Это гарантирует, что коллекция будет как можно более новой.</span><span class="sxs-lookup"><span data-stu-id="e547d-114">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="e547d-115">С другой стороны, использование Обновления может излишне замедлять производительность.</span><span class="sxs-lookup"><span data-stu-id="e547d-115">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

