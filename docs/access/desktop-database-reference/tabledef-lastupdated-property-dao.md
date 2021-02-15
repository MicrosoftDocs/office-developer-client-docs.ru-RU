---
title: Свойство TableDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 994543132fb5323566bd876da066419d0986bd91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308416"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="74c13-102">Свойство TableDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="74c13-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="74c13-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74c13-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74c13-104">Возвращает дату и время последнего изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="74c13-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="74c13-105">Только для чтения, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="74c13-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c13-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74c13-106">Syntax</span></span>

<span data-ttu-id="74c13-107">*выражение .* LastUpdated</span><span class="sxs-lookup"><span data-stu-id="74c13-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="74c13-108">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="74c13-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="74c13-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74c13-109">Remarks</span></span>

<span data-ttu-id="74c13-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления объекта.</span><span class="sxs-lookup"><span data-stu-id="74c13-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="74c13-111">В многомерной среде пользователи должны получить эти параметры непосредственно с файлового сервера, чтобы избежать несоответствий в параметрах свойств DateCreated и LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="74c13-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

