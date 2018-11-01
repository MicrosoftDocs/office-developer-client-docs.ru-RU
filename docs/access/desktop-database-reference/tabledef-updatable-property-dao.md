---
title: TableDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4908699aaea69a001a1abd3761b78607ae2640a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869822"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="cd122-102">TableDef.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="cd122-102">TableDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="cd122-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd122-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd122-104">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="cd122-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="cd122-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="cd122-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd122-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd122-106">Syntax</span></span>

<span data-ttu-id="cd122-107">*выражение* . Обновляемые</span><span class="sxs-lookup"><span data-stu-id="cd122-107">*expression* .Updatable</span></span>

<span data-ttu-id="cd122-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="cd122-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd122-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="cd122-109">Remarks</span></span>

<span data-ttu-id="cd122-110">Настройка свойства **с возможностью записи** всегда является **True** для только что созданный объект **TableDef** и **значение False** для связанного объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="cd122-110">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object.</span></span> <span data-ttu-id="cd122-111">Новый объект **TableDef** могут быть добавлены только базы данных, для которого у текущего пользователя есть разрешение на запись.</span><span class="sxs-lookup"><span data-stu-id="cd122-111">A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

