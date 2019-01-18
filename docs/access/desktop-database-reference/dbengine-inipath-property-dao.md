---
title: Свойство DBEngine.IniPath (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717631"
---
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="9f5aa-102">Свойство DBEngine.IniPath (DAO)</span><span class="sxs-lookup"><span data-stu-id="9f5aa-102">DBEngine.IniPath property (DAO)</span></span>


<span data-ttu-id="9f5aa-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f5aa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f5aa-104">Задает или возвращает сведения о раздел реестра Windows, который содержит значения для ядро базы данных Microsoft Access (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9f5aa-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f5aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f5aa-105">Syntax</span></span>

<span data-ttu-id="9f5aa-106">*выражение* . IniPath</span><span class="sxs-lookup"><span data-stu-id="9f5aa-106">*expression* .IniPath</span></span>

<span data-ttu-id="9f5aa-107">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="9f5aa-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f5aa-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="9f5aa-108">Remarks</span></span>

<span data-ttu-id="9f5aa-109">Ядро базы данных Microsoft Access можно настроить с помощью реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="9f5aa-109">You can configure the Microsoft Access database engine with the Windows Registry.</span></span> <span data-ttu-id="9f5aa-110">Реестра можно использовать для установки параметров, таких как устанавливаемый драйвер ISAM библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="9f5aa-110">You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="9f5aa-111">Для этого параметра не влияет на необходимо задать свойство **IniPath** перед приложение вызывает другой код DAO.</span><span class="sxs-lookup"><span data-stu-id="9f5aa-111">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code.</span></span> <span data-ttu-id="9f5aa-112">Область этот параметр не может превышать приложения и не могут быть изменены без перезапуска приложения.</span><span class="sxs-lookup"><span data-stu-id="9f5aa-112">The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="9f5aa-113">Можно также с помощью реестра предоставляют параметры инициализации для некоторых устанавливаемый драйвер ISAM драйверов базы данных.</span><span class="sxs-lookup"><span data-stu-id="9f5aa-113">You also use the Registry to provide initialization parameters for some installable ISAM database drivers.</span></span> <span data-ttu-id="9f5aa-114">Например для использования Paradox версии 4.0, присвойте свойству **IniPath** часть реестра с соответствующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="9f5aa-114">For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="9f5aa-115">Это свойство определяет либо HKEY\_ЛОКАЛЬНОГО\_компьютера или HKEY\_ЛОКАЛЬНОГО\_пользователя.</span><span class="sxs-lookup"><span data-stu-id="9f5aa-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="9f5aa-116">Если ключ не корневые предоставлен, значение по умолчанию — HKEY\_ЛОКАЛЬНОГО\_компьютера.</span><span class="sxs-lookup"><span data-stu-id="9f5aa-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>

