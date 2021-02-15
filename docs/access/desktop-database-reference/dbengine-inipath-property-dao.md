---
title: DBEngine.IniPath (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f14f9f2d028bb8a9a8e71bc9d7b97ea5672466f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294297"
---
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="fcae5-102">DBEngine.IniPath (DAO)</span><span class="sxs-lookup"><span data-stu-id="fcae5-102">DBEngine.IniPath property (DAO)</span></span>


<span data-ttu-id="fcae5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcae5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fcae5-104">Задает или возвращает сведения о ключе реестра Windows, который содержит значения для ядвижка базы данных Microsoft Access (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fcae5-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="fcae5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcae5-105">Syntax</span></span>

<span data-ttu-id="fcae5-106">*выражение .* IniPath</span><span class="sxs-lookup"><span data-stu-id="fcae5-106">*expression* .IniPath</span></span>

<span data-ttu-id="fcae5-107">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="fcae5-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcae5-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="fcae5-108">Remarks</span></span>

<span data-ttu-id="fcae5-109">Вы можете настроить яд базы данных Microsoft Access с помощью реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="fcae5-109">You can configure the Microsoft Access database engine with the Windows Registry.</span></span> <span data-ttu-id="fcae5-110">Реестр можно использовать для установки параметров, таких как устанавливаемые DLL ISAM.</span><span class="sxs-lookup"><span data-stu-id="fcae5-110">You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="fcae5-111">Чтобы этот параметр вступил в силу, необходимо установить свойство **IniPath,** прежде чем приложение будет вызывать любой другой код DAO.</span><span class="sxs-lookup"><span data-stu-id="fcae5-111">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code.</span></span> <span data-ttu-id="fcae5-112">Область действия этого параметра ограничена приложением и не может быть изменена без перезапуска приложения.</span><span class="sxs-lookup"><span data-stu-id="fcae5-112">The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="fcae5-113">Реестр также используется для предоставления параметров инициализации для некоторых устанавливаемых драйверов базы данных ISAM.</span><span class="sxs-lookup"><span data-stu-id="fcae5-113">You also use the Registry to provide initialization parameters for some installable ISAM database drivers.</span></span> <span data-ttu-id="fcae5-114">Например, чтобы использовать Paradox версии 4.0, установите для свойства **IniPath** часть реестра, содержащую соответствующие параметры.</span><span class="sxs-lookup"><span data-stu-id="fcae5-114">For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="fcae5-115">Это свойство распознает HKEY \_ LOCAL \_ MACHINE или HKEY \_ LOCAL \_ USER.</span><span class="sxs-lookup"><span data-stu-id="fcae5-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="fcae5-116">Если корневой ключ не задается, по умолчанию задается HKEY \_ LOCAL \_ MACHINE.</span><span class="sxs-lookup"><span data-stu-id="fcae5-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>

