---
title: Макрокоманда RestoreWindow
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 35637781035b7a449ba574cf5f6c84f2cb5223db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306589"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="7e034-102">Макрокоманда RestoreWindow</span><span class="sxs-lookup"><span data-stu-id="7e034-102">RestoreWindow macro action</span></span>

<span data-ttu-id="7e034-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e034-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e034-104">Вы можете использовать действие **ресторевиндов** для восстановления предыдущего размера развернутого или свернутого окна.</span><span class="sxs-lookup"><span data-stu-id="7e034-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>

> [!NOTE]
> <span data-ttu-id="7e034-105">Это действие невозможно применить к окнам кода в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7e034-105">This action can't be applied to code windows in the Visual Basic Editor.</span></span> <span data-ttu-id="7e034-106">Сведения о том, как повлиять на окна кода, представлены в разделе свойство **WindowState** .</span><span class="sxs-lookup"><span data-stu-id="7e034-106">For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="7e034-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="7e034-107">Setting</span></span>

<span data-ttu-id="7e034-108">Макрокоманда **ресторевиндов** не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="7e034-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e034-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e034-109">Remarks</span></span>

<span data-ttu-id="7e034-110">Это действие выполняется для выбранного объекта.</span><span class="sxs-lookup"><span data-stu-id="7e034-110">This action works on the selected object.</span></span> <span data-ttu-id="7e034-111">Если объект свернут, его можно сначала выбрать с помощью макрокоманды **ВыделитьОбъект (SelectObject** ), а затем восстановить до его предыдущего размера с помощью действия **ресторевиндов** .</span><span class="sxs-lookup"><span data-stu-id="7e034-111">If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="7e034-112">Вы можете использовать действие **мовеандсизевиндов** для перемещения или изменения размера восстановленного окна.</span><span class="sxs-lookup"><span data-stu-id="7e034-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="7e034-113">Действие **ресторевиндов** имеет тот же результат, что и нажатие кнопки " **восстановить** " в правом верхнем углу окна или нажатие команды " **восстановить** " **в оконном меню окна** .</span><span class="sxs-lookup"><span data-stu-id="7e034-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="7e034-114">Чтобы запустить действие **ресторевиндов** в модуле Visual Basic для приложений (VBA), используйте метод **RESTORE** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="7e034-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

