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
ms.openlocfilehash: dfd7877ff1db960afcbf864f1e72ff01b12e8f09
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998954"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="64350-102">Макрокоманда RestoreWindow</span><span class="sxs-lookup"><span data-stu-id="64350-102">RestoreWindow macro action</span></span>

<span data-ttu-id="64350-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64350-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64350-104">Действие **RestoreWindow** можно использовать для восстановления предыдущих размеров развернутого или свернутого окна.</span><span class="sxs-lookup"><span data-stu-id="64350-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>

> [!NOTE]
> <span data-ttu-id="64350-105">Это действие не может применяться к windows кода в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="64350-105">This action can't be applied to code windows in the Visual Basic Editor.</span></span> <span data-ttu-id="64350-106">Для получения сведений о действиях с кодом windows приведены в разделе свойство **WindowState** .</span><span class="sxs-lookup"><span data-stu-id="64350-106">For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="64350-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="64350-107">Setting</span></span>

<span data-ttu-id="64350-108">Действие **RestoreWindow** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="64350-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="64350-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="64350-109">Remarks</span></span>

<span data-ttu-id="64350-110">Это действие работает на выбранный объект.</span><span class="sxs-lookup"><span data-stu-id="64350-110">This action works on the selected object.</span></span> <span data-ttu-id="64350-111">При свернутых объекта можно выбрать ее с помощью **ВыделитьОбъект** и последующее восстановление предыдущих размеров с помощью действия **RestoreWindow** .</span><span class="sxs-lookup"><span data-stu-id="64350-111">If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="64350-112">Чтобы переместить или изменить ее размер окна, после восстановления можно использовать действие **MoveAndSizeWindow** .</span><span class="sxs-lookup"><span data-stu-id="64350-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="64350-113">Действие **RestoreWindow** имеет тот же эффект, как нажать кнопку " **Восстановление** " в правом верхнем углу окна или выбрав команду **восстановить** в **элемент управления** меню.</span><span class="sxs-lookup"><span data-stu-id="64350-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="64350-114">Чтобы выполнить действие **RestoreWindow** в Visual Basic для приложений (VBA) модуль, используйте метод **восстановления** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="64350-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

