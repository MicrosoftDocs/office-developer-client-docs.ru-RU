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
ms.openlocfilehash: fd744f10d212d8ff0f7c78ca72781869ccdcd57e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928763"
---
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="f9ce3-102">Свойство DBEngine.IniPath (DAO)</span><span class="sxs-lookup"><span data-stu-id="f9ce3-102">DBEngine.IniPath property (DAO)</span></span>


<span data-ttu-id="f9ce3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9ce3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9ce3-104">Задает или возвращает сведения о раздел реестра Windows, который содержит значения для ядро базы данных Microsoft Access (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f9ce3-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9ce3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9ce3-105">Syntax</span></span>

<span data-ttu-id="f9ce3-106">*выражение* . IniPath</span><span class="sxs-lookup"><span data-stu-id="f9ce3-106">*expression* .IniPath</span></span>

<span data-ttu-id="f9ce3-107">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="f9ce3-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9ce3-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="f9ce3-108">Remarks</span></span>

<span data-ttu-id="f9ce3-109">Ядро базы данных Microsoft Access можно настроить с помощью реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="f9ce3-109">You can configure the Microsoft Access databse engine with the Windows Registry.</span></span> <span data-ttu-id="f9ce3-110">Реестра можно использовать для установки параметров, таких как устанавливаемый драйвер ISAM библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="f9ce3-110">You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="f9ce3-111">Для этого параметра не влияет на необходимо задать свойство **IniPath** перед приложение вызывает другой код DAO.</span><span class="sxs-lookup"><span data-stu-id="f9ce3-111">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code.</span></span> <span data-ttu-id="f9ce3-112">Область этот параметр не может превышать приложения и не могут быть изменены без перезапуска приложения.</span><span class="sxs-lookup"><span data-stu-id="f9ce3-112">The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="f9ce3-113">Можно также с помощью реестра предоставляют параметры инициализации для некоторых устанавливаемый драйвер ISAM драйверов базы данных.</span><span class="sxs-lookup"><span data-stu-id="f9ce3-113">You also use the Registry to provide initialization parameters for some installable ISAM database drivers.</span></span> <span data-ttu-id="f9ce3-114">Например для использования Paradox версии 4.0, присвойте свойству **IniPath** часть реестра с соответствующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="f9ce3-114">For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="f9ce3-115">Это свойство определяет либо HKEY\_ЛОКАЛЬНОГО\_компьютера или HKEY\_ЛОКАЛЬНОГО\_пользователя.</span><span class="sxs-lookup"><span data-stu-id="f9ce3-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="f9ce3-116">Если ключ не корневые предоставлен, значение по умолчанию — HKEY\_ЛОКАЛЬНОГО\_компьютера.</span><span class="sxs-lookup"><span data-stu-id="f9ce3-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>

