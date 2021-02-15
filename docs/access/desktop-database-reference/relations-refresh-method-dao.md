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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306771"
---
# <a name="relationsrefresh-method-dao"></a><span data-ttu-id="1233a-102">Метод Relations.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="1233a-102">Relations.Refresh method (DAO)</span></span>


<span data-ttu-id="1233a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1233a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1233a-104">Обновляет объекты в указанном уровне, чтобы отразить текущую схему базы данных.</span><span class="sxs-lookup"><span data-stu-id="1233a-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="1233a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1233a-105">Syntax</span></span>

<span data-ttu-id="1233a-106">*выражение .* Обновление</span><span class="sxs-lookup"><span data-stu-id="1233a-106">*expression* .Refresh</span></span>

<span data-ttu-id="1233a-107">*выражение* Переменная, представляюная объект **Relations.**</span><span class="sxs-lookup"><span data-stu-id="1233a-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1233a-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="1233a-108">Remarks</span></span>

<span data-ttu-id="1233a-109">Используйте метод **Refresh** в многомерных средах, в которых другие пользователи могут изменить базу данных.</span><span class="sxs-lookup"><span data-stu-id="1233a-109">Use the **Refresh** method in multiuser environments in which other users may change the database.</span></span> <span data-ttu-id="1233a-110">Кроме того, может потребоваться использовать его в любых коллекциях, на которые косвенно влияют изменения базы данных.</span><span class="sxs-lookup"><span data-stu-id="1233a-110">You may also need to use it on any collections that are indirectly affected by changes to the database.</span></span> <span data-ttu-id="1233a-111">Например, при изменении коллекции **Users** может потребоваться обновить коллекцию **Groups** перед ее **использованием.**</span><span class="sxs-lookup"><span data-stu-id="1233a-111">For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="1233a-112">Коллекция заполняется объектами при первом ссылке и не отражает автоматически последующие изменения, внесенные другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="1233a-112">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make.</span></span> <span data-ttu-id="1233a-113">Если, скорее всего, другой пользователь изменил коллекцию, используйте метод Refresh в коллекции непосредственно перед тем, как выполнять любую задачу в приложении, предполагая наличие или отсутствие определенного объекта в коллекции.</span><span class="sxs-lookup"><span data-stu-id="1233a-113">If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection.</span></span> <span data-ttu-id="1233a-114">Это гарантирует, что коллекция будет как можно более новой.</span><span class="sxs-lookup"><span data-stu-id="1233a-114">This will ensure that the collection is as up-to-date as possible.</span></span> <span data-ttu-id="1233a-115">С другой стороны, использование refresh может привести к излишнему замедлению производительности.</span><span class="sxs-lookup"><span data-stu-id="1233a-115">On the other hand, using Refresh can unnecessarily slow performance.</span></span>

