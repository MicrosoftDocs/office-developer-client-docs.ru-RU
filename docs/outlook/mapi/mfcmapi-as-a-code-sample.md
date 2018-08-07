---
title: Mfcmapi (en) в качестве примера кода
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fc92cc8deb3d12c4bc8fca4c680fd4a675b4a578
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810015"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="195b5-103">Mfcmapi (en) в качестве примера кода</span><span class="sxs-lookup"><span data-stu-id="195b5-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="195b5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="195b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="195b5-105">Пример mfcmapi (en) использует API системы обмена сообщениями для предоставления доступа к хранилищам MAPI через графический интерфейс пользователя.</span><span class="sxs-lookup"><span data-stu-id="195b5-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="195b5-106">После загрузки в этом примере исходные файлы можно использовать для проверки случаев использования пример для многих интерфейсов MAPI и справочные материалы.</span><span class="sxs-lookup"><span data-stu-id="195b5-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="195b5-107">Для получения дополнительных сведений см. [MAPI](mapi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="195b5-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="195b5-108">Платформы:</span><span class="sxs-lookup"><span data-stu-id="195b5-108">Platforms:</span></span>  <br/> |<span data-ttu-id="195b5-109">Microsoft Visual Studio 2008 для компиляции для Windows 7, Windows Vista, Windows Server 2008, Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="195b5-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="195b5-110">Чтобы загрузить mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="195b5-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="195b5-111">На странице [mfcmapi (en)](http://codeplex.com/MFCMAPI) перейдите на вкладку **Исходный код** .</span><span class="sxs-lookup"><span data-stu-id="195b5-111">On the [MFCMAPI](http://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="195b5-112">В разделе **Последние возврата**нажмите кнопку **загрузить** для последнего построения.</span><span class="sxs-lookup"><span data-stu-id="195b5-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="195b5-113">Прочтите лицензионное соглашение и нажмите кнопку **я принимаю**.</span><span class="sxs-lookup"><span data-stu-id="195b5-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="195b5-114">В диалоговом окне **Загрузка файла** нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="195b5-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="195b5-115">В диалоговом окне **Сохранить как** выберите папку, в которой требуется сохранить исходные файлы и нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="195b5-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="195b5-116">В диалоговом окне **Загрузка завершена** щелкните **Открыть папку**.</span><span class="sxs-lookup"><span data-stu-id="195b5-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="195b5-117">Можно нажать кнопку **Закрыть** , чтобы закрыть диалоговое окно и найдите ZIP-исходные файлы в папке, сохраненный в.</span><span class="sxs-lookup"><span data-stu-id="195b5-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="195b5-118">Щелкните правой кнопкой мыши **mfcmapi (en) —\<номер версии\>.zip** файла и нажмите кнопку **Извлечь все**.</span><span class="sxs-lookup"><span data-stu-id="195b5-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="195b5-119">В диалоговом окне, которое отображается нажмите кнопку **извлечь** для извлечения файлов в папку, которая отображается.</span><span class="sxs-lookup"><span data-stu-id="195b5-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="195b5-120">Можно нажать кнопку **Обзор** , выберите или создайте другую папку.</span><span class="sxs-lookup"><span data-stu-id="195b5-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="195b5-121">Запустите Visual Studio 2008 с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="195b5-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="195b5-122">Если компьютер работает под управлением Windows XP, вы должны войти в систему с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="195b5-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="195b5-123">Если компьютер работает под управлением ОС Windows Vista, вы должны войти в систему с правами администратора и необходимо щелкните правой кнопкой мыши значок Visual Studio 2008 и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="195b5-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="195b5-124">В Visual Studio 2008 откройте меню **файл**, выберите пункт **Открыть**и выберите **Проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="195b5-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="195b5-125">Перейдите к папке, в которой вы сохранили примера, выберите **MFCMapi.vcproj**и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="195b5-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="195b5-126">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="195b5-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="195b5-127">В диалоговом окне **Сохранение файла** нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="195b5-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="195b5-128">Для использования в качестве примера кода mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="195b5-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="195b5-129">В **Обозревателе решений**разверните узел проекта **mfcmapi (en)** и просматривать файлы в узлах, **Файлы заголовков**, **Файлов ресурсов**и **Исходных файлов** для программирования сценариев.</span><span class="sxs-lookup"><span data-stu-id="195b5-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="195b5-130">Многие разделы метод в разделе [Интерфейсов MAPI](mapi-interfaces.md) укажите исходные файлы mfcmapi (en) для примеры программного кода.</span><span class="sxs-lookup"><span data-stu-id="195b5-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="195b5-131">Например в [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) указания откроете функцию `CMsgStoreDlg::OnDisplayReceiveFolderTable` в файле MsgStoreDlg.cpp.</span><span class="sxs-lookup"><span data-stu-id="195b5-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="195b5-132">См. также</span><span class="sxs-lookup"><span data-stu-id="195b5-132">See also</span></span>

- [<span data-ttu-id="195b5-133">Примеры MAPI</span><span class="sxs-lookup"><span data-stu-id="195b5-133">MAPI Samples</span></span>](mapi-samples.md)

