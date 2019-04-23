---
title: Свойство TableDef. DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5dc326b271e8444211bba0cd2d3c37c047ac205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314541"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="4cf4c-102">Свойство TableDef. DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="4cf4c-102">TableDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="4cf4c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4cf4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4cf4c-104">Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4cf4c-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="4cf4c-105">Только для чтения, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="4cf4c-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf4c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cf4c-106">Syntax</span></span>

<span data-ttu-id="4cf4c-107">*Expression* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="4cf4c-107">*expression* .DateCreated</span></span>

<span data-ttu-id="4cf4c-108">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="4cf4c-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cf4c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cf4c-109">Remarks</span></span>

<span data-ttu-id="4cf4c-110">**DateCreated** и **ластупдатед** возвращают дату и время создания или последнего обновления объекта.</span><span class="sxs-lookup"><span data-stu-id="4cf4c-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="4cf4c-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно с файлового сервера, чтобы избежать расхождений в параметрах свойств DateCreated и Ластупдатед.</span><span class="sxs-lookup"><span data-stu-id="4cf4c-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

