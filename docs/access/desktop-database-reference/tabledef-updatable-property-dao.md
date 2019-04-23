---
title: Свойство TableDef. обновляющей (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314415"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="8eb82-102">Свойство TableDef. обновляющей (DAO)</span><span class="sxs-lookup"><span data-stu-id="8eb82-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="8eb82-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8eb82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8eb82-104">Возвращает значение, которое указывает на то, можно ли изменить DAO объект.</span><span class="sxs-lookup"><span data-stu-id="8eb82-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="8eb82-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="8eb82-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb82-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8eb82-106">Syntax</span></span>

<span data-ttu-id="8eb82-107">*Expression* . Updatable</span><span class="sxs-lookup"><span data-stu-id="8eb82-107">*expression* .Updatable</span></span>

<span data-ttu-id="8eb82-108">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="8eb82-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eb82-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8eb82-109">Remarks</span></span>

<span data-ttu-id="8eb82-110">Параметр **обновляемое** свойство всегда имеет **значение true** для вновь созданного объекта **tabledef** и **значение false** для связанного объекта **tabledef** .</span><span class="sxs-lookup"><span data-stu-id="8eb82-110">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object.</span></span> <span data-ttu-id="8eb82-111">Новый объект **tabledef** можно добавить только в базу данных, для которой текущий пользователь имеет разрешение на запись.</span><span class="sxs-lookup"><span data-stu-id="8eb82-111">A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

