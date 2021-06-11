---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406026"
---
# <a name="openstreamonfilew"></a><span data-ttu-id="33246-103">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="33246-103">OpenStreamOnFileW</span></span>

  
  
<span data-ttu-id="33246-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33246-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33246-105">Выделяет и инициализирует объект OLE **IStream** для доступа к содержимому файла.</span><span class="sxs-lookup"><span data-stu-id="33246-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="33246-106">Эта функция принимает строки UNICODE в качестве аргументов, в отличие от версии ANSI этой функции [OpenStreamOnFile,](openstreamonfile.md)и, таким образом, позволяет использовать произвольные символы в имени файла, включая путь и расширение файла.</span><span class="sxs-lookup"><span data-stu-id="33246-106">This function takes UNICODE strings as arguments, unlike the ANSI version of this function [OpenStreamOnFile](openstreamonfile.md), and thus allows for arbitrary characters in the file name including the path and file extension.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33246-107">Экспортируемая по:</span><span class="sxs-lookup"><span data-stu-id="33246-107">Exported by:</span></span>  <br/> |<span data-ttu-id="33246-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="33246-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="33246-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="33246-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="33246-110">Outlook</span><span class="sxs-lookup"><span data-stu-id="33246-110">Outlook</span></span>  <br/> |
|<span data-ttu-id="33246-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="33246-111">Called by:</span></span>  <br/> |<span data-ttu-id="33246-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="33246-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="33246-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="33246-113">Parameters</span></span>

 <span data-ttu-id="33246-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="33246-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="33246-115">[in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="33246-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="33246-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="33246-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="33246-117">[in] Указатель на функцию [MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться для бесплатной памяти.</span><span class="sxs-lookup"><span data-stu-id="33246-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="33246-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="33246-118">_ulFlags_</span></span>
  
> <span data-ttu-id="33246-119">[in] Битмаски флагов, используемых для управления созданием или открытием файла, к нему можно получить доступ через объект OLE **IStream.**</span><span class="sxs-lookup"><span data-stu-id="33246-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="33246-120">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="33246-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="33246-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="33246-121">SOF_UNIQUEFILENAME</span></span>
  
> <span data-ttu-id="33246-122">Для объекта IStream должен быть создан **временный** файл.</span><span class="sxs-lookup"><span data-stu-id="33246-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="33246-123">Если этот флаг заданной, STGM_CREATE и STGM_READWRITE должны быть заданной.</span><span class="sxs-lookup"><span data-stu-id="33246-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="33246-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="33246-124">STGM_CREATE</span></span>
  
> <span data-ttu-id="33246-125">Файл должен быть создан, даже если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="33246-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="33246-126">Если параметр  _lpszFileName_ не задан, необходимо STGM_DELETEONRELEASE этот флаг.</span><span class="sxs-lookup"><span data-stu-id="33246-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="33246-127">Если STGM_CREATE установлено, STGM_READWRITE должен быть также установлен флаг.</span><span class="sxs-lookup"><span data-stu-id="33246-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="33246-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="33246-128">STGM_DELETEONRELEASE</span></span>
  
> <span data-ttu-id="33246-129">Файл должен быть удален после выпуска **объекта IStream.**</span><span class="sxs-lookup"><span data-stu-id="33246-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="33246-130">Если параметр  _lpszFileName_ не задан, необходимо STGM_CREATE этот флаг.</span><span class="sxs-lookup"><span data-stu-id="33246-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="33246-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="33246-131">STGM_READ</span></span>
  
> <span data-ttu-id="33246-132">Файл должен быть создан или открыт с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="33246-132">The file is to be created or opened with read-only access.</span></span>
    
<span data-ttu-id="33246-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="33246-133">STGM_READWRITE</span></span>
  
> <span data-ttu-id="33246-134">Файл должен быть создан или открыт с разрешения на чтение и написание.</span><span class="sxs-lookup"><span data-stu-id="33246-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="33246-135">Если этот флаг не установлен, STGM_CREATE не должен быть заданной.</span><span class="sxs-lookup"><span data-stu-id="33246-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span>
    
 <span data-ttu-id="33246-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="33246-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="33246-137">[in] Имя файла, включая путь и расширение, файла с именем Unicode, для которого **OpenStreamOnFileW** инициализирует **объект IStream.**</span><span class="sxs-lookup"><span data-stu-id="33246-137">[in] The filename, including path and extension, of the Unicode named file for which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="33246-138">Если флаг SOF_UNIQUEFILENAME,  _lpszFileName_ содержит путь к каталогу, в котором создается временный файл.</span><span class="sxs-lookup"><span data-stu-id="33246-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="33246-139">Если  _lpszFileName_ является NULL, **OpenStreamOnFileW** получает соответствующий путь из системы, и необходимо установить STGM_CREATE и STGM_DELETEONRELEASE флаги.</span><span class="sxs-lookup"><span data-stu-id="33246-139">If  _lpszFileName_ is NULL, **OpenStreamOnFileW** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="33246-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="33246-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="33246-141">[in] Префикс для имени файла Unicode, на котором **OpenStreamOnFileW** инициализирует **объект IStream.**</span><span class="sxs-lookup"><span data-stu-id="33246-141">[in] The prefix for the Unicode filename on which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="33246-142">Если установлено, префикс должен содержать не более трех символов.</span><span class="sxs-lookup"><span data-stu-id="33246-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="33246-143">Если  _lpszPrefix_ является NULL, используется префикс "SOF".</span><span class="sxs-lookup"><span data-stu-id="33246-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="33246-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="33246-144">_lppStream_</span></span>
  
> <span data-ttu-id="33246-145">[вышел] Указатель на указатель на объект, подвергая обнажаемой **интерфейсу IStream.**</span><span class="sxs-lookup"><span data-stu-id="33246-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="33246-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33246-146">Return value</span></span>

<span data-ttu-id="33246-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="33246-147">S_OK</span></span>
  
> <span data-ttu-id="33246-148">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="33246-148">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="33246-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="33246-149">MAPI_E_NO_ACCESS</span></span>
  
> <span data-ttu-id="33246-150">Доступ к файлу был недостаточен из-за недостаточного количества разрешений пользователей или из-за невозможного изменения файлов, доступных только для чтения.</span><span class="sxs-lookup"><span data-stu-id="33246-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span>
    
<span data-ttu-id="33246-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="33246-151">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="33246-152">Назначенный файл не существует.</span><span class="sxs-lookup"><span data-stu-id="33246-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="33246-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="33246-153">Remarks</span></span>

<span data-ttu-id="33246-154">Функция **OpenStreamOnFileW** имеет два важных использования в дополнение к обработке файла с именем Unicode, отличаемого параметром флага SOF_UNIQUEFILENAME.</span><span class="sxs-lookup"><span data-stu-id="33246-154">The **OpenStreamOnFileW** function has two important uses in addition to handling a file with a Unicode name, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="33246-155">Если этот флаг не установлен, **OpenStreamOnFileW** открывает объект **IStream** в существующем файле, например для копирования его содержимого в свойство [PR_ATTACH_DATA_BIN (PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)вложения с помощью метода **IStream::CopyTo.** </span><span class="sxs-lookup"><span data-stu-id="33246-155">When this flag is not set, **OpenStreamOnFileW** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="33246-156">В этом случае  _параметр lpszFileName_ указывает путь и имя файла файла.</span><span class="sxs-lookup"><span data-stu-id="33246-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="33246-157">Когда SOF_UNIQUEFILENAME установлено, **OpenStreamOnFileW** создает временный файл для хранения данных для **объекта IStream.**</span><span class="sxs-lookup"><span data-stu-id="33246-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFileW** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="33246-158">Для этого использования параметр  _lpszFileName_ может необязательно назначать путь к каталогу, в котором должен быть создан файл, а параметр  _lpszPrefix_ может дополнительно указать префикс для имени файла.</span><span class="sxs-lookup"><span data-stu-id="33246-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="33246-159">После завершения работы клиентского приложения или поставщика услуг с объектом **IStream** необходимо освободить его, позвонив методу OLE **IStream::Release.**</span><span class="sxs-lookup"><span data-stu-id="33246-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="33246-160">MAPI использует функции, на которые указывают  _lpAllocateBuffer_ и  _lpFreeBuffer_ для большинства распределений памяти и распределения, в частности для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="33246-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="33246-161">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="33246-161">Notes to callers</span></span>

<span data-ttu-id="33246-162">Флаг SOF_UNIQUEFILENAME используется для создания временного файла с именем, уникальным для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="33246-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="33246-163">Если этот флаг задан, параметр  _lpszFileName_ заметив путь для временного файла, а параметр  _lpszPrefix_ содержит символы префикса имени файла.</span><span class="sxs-lookup"><span data-stu-id="33246-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="33246-164">Построенное имя файла — <prefix> это HHHH. TMP, где HHHH — это гексадецимальное число.</span><span class="sxs-lookup"><span data-stu-id="33246-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="33246-165">Если _lpszFileName_ является NULL, файл будет создан во временном каталоге файлов, который возвращается из функции **Windows GetTempPath** или текущего каталога, если не назначен временный каталог файлов.</span><span class="sxs-lookup"><span data-stu-id="33246-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span>
  
<span data-ttu-id="33246-166">Если флаг SOF_UNIQUEFILENAME не установлен,  _lpszPrefix_ игнорируется, а  _lpszFileName_ должен содержать полностью квалифицированный путь и имя файла для открытия или создания файла.</span><span class="sxs-lookup"><span data-stu-id="33246-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="33246-167">Файл будет открыт или создан на основе других флагов, установленных в  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="33246-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33246-168">См. также</span><span class="sxs-lookup"><span data-stu-id="33246-168">See also</span></span>



[<span data-ttu-id="33246-169">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="33246-169">OpenStreamOnFile</span></span>](openstreamonfile.md)

