---
title: Свойство DBEngine. IniPath (DAO)
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
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="39ee5-102">Свойство DBEngine. IniPath (DAO)</span><span class="sxs-lookup"><span data-stu-id="39ee5-102">DBEngine.IniPath property (DAO)</span></span>


<span data-ttu-id="39ee5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39ee5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39ee5-104">Задает или возвращает сведения о разделе реестра Windows, который содержит значения для ядра СУБД Microsoft Access (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="39ee5-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="39ee5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39ee5-105">Syntax</span></span>

<span data-ttu-id="39ee5-106">*Expression* . IniPath</span><span class="sxs-lookup"><span data-stu-id="39ee5-106">*expression* .IniPath</span></span>

<span data-ttu-id="39ee5-107">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="39ee5-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="39ee5-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="39ee5-108">Remarks</span></span>

<span data-ttu-id="39ee5-109">Вы можете настроить ядро СУБД Microsoft Access с помощью реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="39ee5-109">You can configure the Microsoft Access database engine with the Windows Registry.</span></span> <span data-ttu-id="39ee5-110">Вы можете использовать реестр для установки параметров, таких как устанавливаемые библиотеки ISAM DLL.</span><span class="sxs-lookup"><span data-stu-id="39ee5-110">You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="39ee5-111">Чтобы этот параметр действовал, необходимо задать свойство **IniPath** , прежде чем приложение вызовет любой другой код DAO.</span><span class="sxs-lookup"><span data-stu-id="39ee5-111">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code.</span></span> <span data-ttu-id="39ee5-112">Область этого параметра ограничена приложением и не может быть изменена без перезапуска приложения.</span><span class="sxs-lookup"><span data-stu-id="39ee5-112">The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="39ee5-113">Вы также можете использовать реестр для предоставления параметров инициализации для некоторых устанавливаемых драйверов базы данных ISAM.</span><span class="sxs-lookup"><span data-stu-id="39ee5-113">You also use the Registry to provide initialization parameters for some installable ISAM database drivers.</span></span> <span data-ttu-id="39ee5-114">Например, чтобы использовать Paradox версии 4,0, присвойте свойству **IniPath** часть реестра, содержащую соответствующие параметры.</span><span class="sxs-lookup"><span data-stu-id="39ee5-114">For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="39ee5-115">Это свойство распознает либо\_\_локальный\_пользователь, либо\_локальный пользователь hKey.</span><span class="sxs-lookup"><span data-stu-id="39ee5-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="39ee5-116">Если корневой ключ не указан, по умолчанию используется\_локальный\_компьютер hKey.</span><span class="sxs-lookup"><span data-stu-id="39ee5-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>

