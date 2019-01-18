---
title: Свойство TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725975"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="500c9-102">Свойство TableDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="500c9-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="500c9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="500c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="500c9-104">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="500c9-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="500c9-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="500c9-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="500c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="500c9-106">Syntax</span></span>

<span data-ttu-id="500c9-107">*выражение* . Обновляемые</span><span class="sxs-lookup"><span data-stu-id="500c9-107">*expression* .Updatable</span></span>

<span data-ttu-id="500c9-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="500c9-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="500c9-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="500c9-109">Remarks</span></span>

<span data-ttu-id="500c9-110">Настройка свойства **с возможностью записи** всегда является **True** для только что созданный объект **TableDef** и **значение False** для связанного объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="500c9-110">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object.</span></span> <span data-ttu-id="500c9-111">Новый объект **TableDef** могут быть добавлены только базы данных, для которого у текущего пользователя есть разрешение на запись.</span><span class="sxs-lookup"><span data-stu-id="500c9-111">A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

