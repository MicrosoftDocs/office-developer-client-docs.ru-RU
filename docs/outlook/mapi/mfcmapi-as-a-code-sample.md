---
title: MFCMAPI как пример кода
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356863"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="827b8-103">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="827b8-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="827b8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="827b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="827b8-105">В примере MFCMAPI используется API обмена сообщениями для предоставления доступа к хранилищам MAPI с помощью графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="827b8-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="827b8-106">После загрузки этого примера можно использовать исходные файлы для изучения примеров использования для многих интерфейсов и ссылок MAPI.</span><span class="sxs-lookup"><span data-stu-id="827b8-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="827b8-107">Дополнительные сведения см. в [mapi Interfaces.](mapi-interfaces.md)</span><span class="sxs-lookup"><span data-stu-id="827b8-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="827b8-108">Платформы:</span><span class="sxs-lookup"><span data-stu-id="827b8-108">Platforms:</span></span>  <br/> |<span data-ttu-id="827b8-109">Microsoft Visual Studio 2008 Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 и Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="827b8-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="827b8-110">Загрузка MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="827b8-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="827b8-111">На странице [MFCMAPI](https://codeplex.com/MFCMAPI) щелкните **вкладку Исходный код.**</span><span class="sxs-lookup"><span data-stu-id="827b8-111">On the [MFCMAPI](https://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="827b8-112">В **статье Recent Check-Ins** **щелкните Скачать** для последней сборки.</span><span class="sxs-lookup"><span data-stu-id="827b8-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="827b8-113">Прочитайте лицензионный договор, а затем нажмите **кнопку Я согласен**.</span><span class="sxs-lookup"><span data-stu-id="827b8-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="827b8-114">В диалоговом окне **Загрузка файла** щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="827b8-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="827b8-115">В **диалоговом** окне Save As найдите папку, в которой необходимо сохранить исходные файлы, а затем нажмите **кнопку Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="827b8-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="827b8-116">В **диалоговом окне Загрузка полный** щелкните **Открыть папку**.</span><span class="sxs-lookup"><span data-stu-id="827b8-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="827b8-117">Вы также можете щелкнуть **кнопку Закрыть,** чтобы закрыть диалоговое окно и найти файлы источника с молнией в папке, в которую вы их сохранили.</span><span class="sxs-lookup"><span data-stu-id="827b8-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="827b8-118">Щелкните правой кнопкой мыши номер версии **MFCMAPI.zip\< \>** файл, а затем нажмите **кнопку Извлечь все**.</span><span class="sxs-lookup"><span data-stu-id="827b8-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="827b8-119">В отображаемом диалоговом окне нажмите **кнопку** Извлечение, чтобы извлечь файлы в отображаемую папку.</span><span class="sxs-lookup"><span data-stu-id="827b8-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="827b8-120">Вы также можете нажать **кнопку Просмотр,** чтобы выбрать или создать другую папку.</span><span class="sxs-lookup"><span data-stu-id="827b8-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="827b8-121">Выполнить Visual Studio 2008 в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="827b8-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="827b8-122">Если компьютер работает Windows XP, необходимо войти в систему в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="827b8-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="827b8-123">Если компьютер работает Windows Vista, необходимо войти в систему в качестве администратора, а затем щелкнуть правой кнопкой мыши значок Visual Studio 2008 г., а затем нажмите кнопку Выполнить в качестве **администратора.**</span><span class="sxs-lookup"><span data-stu-id="827b8-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="827b8-124">В Visual Studio 2008 нажмите **кнопку Файл**, указать на **открытие,** а затем **нажмите кнопку Project/Solution**.</span><span class="sxs-lookup"><span data-stu-id="827b8-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="827b8-125">Просмотрите расположение, в котором сохранен пример, выберите **MFCMapi.vcproj** и нажмите **кнопку Открыть**.</span><span class="sxs-lookup"><span data-stu-id="827b8-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="827b8-126">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="827b8-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="827b8-127">В **диалоговом окне Сохранить файл как** диалоговое окно нажмите **кнопку Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="827b8-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="827b8-128">Использование MFCMAPI в качестве примера кода</span><span class="sxs-lookup"><span data-stu-id="827b8-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="827b8-129">В **обозревателе** решений расширите **проект MFCMapi** и изучите файлы в узлах **Header Files,** **Resource Files** и **Source Files** для сценариев программирования.</span><span class="sxs-lookup"><span data-stu-id="827b8-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="827b8-130">Многие темы метода в разделе [ИНТЕРФЕЙСЫ MAPI](mapi-interfaces.md) указывают на исходные файлы MFCMAPI для примеров программирования.</span><span class="sxs-lookup"><span data-stu-id="827b8-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="827b8-131">Например, в [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) вам поручено взглянуть на функцию в  `CMsgStoreDlg::OnDisplayReceiveFolderTable` файле MsgStoreDlg.cpp.</span><span class="sxs-lookup"><span data-stu-id="827b8-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="827b8-132">См. также</span><span class="sxs-lookup"><span data-stu-id="827b8-132">See also</span></span>

- [<span data-ttu-id="827b8-133">Примеры MAPI</span><span class="sxs-lookup"><span data-stu-id="827b8-133">MAPI Samples</span></span>](mapi-samples.md)

