---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8c246968dcac719a8ee8177e20e802f9c7033435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810078"
---
# <a name="openstreamonfile"></a><span data-ttu-id="5bac9-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="5bac9-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="5bac9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bac9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bac9-105">Выделяет и инициализирует объект OLE **IStream** для доступа к содержимому файла.</span><span class="sxs-lookup"><span data-stu-id="5bac9-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="5bac9-106">Эта функция принимает строку ANSI, рекомендуется использовать имя файла, включая путь и расширение файла, таким образом, использование Юникод версии этой функции [OpenStreamOnFileW](openstreamonfilew.md).</span><span class="sxs-lookup"><span data-stu-id="5bac9-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bac9-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5bac9-107">Header file:</span></span>  <br/> |<span data-ttu-id="5bac9-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5bac9-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5bac9-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="5bac9-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="5bac9-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="5bac9-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="5bac9-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="5bac9-111">Called by:</span></span>  <br/> |<span data-ttu-id="5bac9-112">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="5bac9-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="5bac9-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="5bac9-113">Parameters</span></span>

 <span data-ttu-id="5bac9-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="5bac9-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="5bac9-115">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="5bac9-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="5bac9-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="5bac9-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="5bac9-117">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="5bac9-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="5bac9-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5bac9-118">_ulFlags_</span></span>
  
> <span data-ttu-id="5bac9-119">[in] Битовая маска, флагов, используемых для управления Создание или открытие файла были доступны с помощью объекта OLE **IStream** .</span><span class="sxs-lookup"><span data-stu-id="5bac9-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="5bac9-120">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="5bac9-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="5bac9-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="5bac9-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="5bac9-122">Временный файл должен быть создан для объекта **IStream** .</span><span class="sxs-lookup"><span data-stu-id="5bac9-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="5bac9-123">Если установлен этот флаг, необходимо также задать флаги STGM_CREATE и STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="5bac9-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="5bac9-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="5bac9-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="5bac9-125">Файл должен быть создан даже в том случае, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="5bac9-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="5bac9-126">Если не задан параметр _lpszFileName_ , как этот флаг, так и в STGM_DELETEONRELEASE должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="5bac9-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="5bac9-127">Если значение STGM_CREATE, необходимо также установить флаг STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="5bac9-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="5bac9-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="5bac9-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="5bac9-129">Удаление после выхода объекта **IStream** — файл.</span><span class="sxs-lookup"><span data-stu-id="5bac9-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="5bac9-130">Если не задан параметр _lpszFileName_ , как этот флаг, так и в STGM_CREATE должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="5bac9-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="5bac9-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="5bac9-131">STGM_READ</span></span> 
  
> <span data-ttu-id="5bac9-132">Файл является создана или открыта с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5bac9-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="5bac9-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="5bac9-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="5bac9-134">Файл является создана или открыта с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="5bac9-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="5bac9-135">Если этот флаг не установлен, флаг STGM_CREATE не должно быть задано либо.</span><span class="sxs-lookup"><span data-stu-id="5bac9-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="5bac9-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="5bac9-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="5bac9-137">[in] Имя файла, включая путь и расширение файла, для которого **OpenStreamOnFile** инициализирует объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="5bac9-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="5bac9-138">Если значение флага SOF_UNIQUEFILENAME, _lpszFileName_ содержит путь к каталогу, в котором следует создать временный файл.</span><span class="sxs-lookup"><span data-stu-id="5bac9-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="5bac9-139">Если _lpszFileName_ имеет значение NULL, **OpenStreamOnFile** получает соответствующий путь из системы и должно быть задано как STGM_CREATE, так и STGM_DELETEONRELEASE флаги.</span><span class="sxs-lookup"><span data-stu-id="5bac9-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="5bac9-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="5bac9-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="5bac9-141">[in] Префикс имени файла, на котором **OpenStreamOnFile** инициализирует объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="5bac9-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="5bac9-142">Если задано, префикс должен содержать не более трех символов.</span><span class="sxs-lookup"><span data-stu-id="5bac9-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="5bac9-143">Если _lpszPrefix_ имеет значение NULL, используется префикс «SOF».</span><span class="sxs-lookup"><span data-stu-id="5bac9-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="5bac9-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="5bac9-144">_lppStream_</span></span>
  
> <span data-ttu-id="5bac9-145">[out] Указатель на указатель на объект, предоставление интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="5bac9-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5bac9-146">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="5bac9-146">Return value</span></span>

<span data-ttu-id="5bac9-147">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="5bac9-147">S_OK</span></span> 
  
> <span data-ttu-id="5bac9-148">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5bac9-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="5bac9-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5bac9-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5bac9-150">Файл недоступен из-за разрешений недостаточно пользователя или из-за нельзя изменять файлы, доступные только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5bac9-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="5bac9-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5bac9-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5bac9-152">Заданный файл не существует.</span><span class="sxs-lookup"><span data-stu-id="5bac9-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bac9-153">Замечания</span><span class="sxs-lookup"><span data-stu-id="5bac9-153">Remarks</span></span>

<span data-ttu-id="5bac9-154">Функция **OpenStreamOnFile** имеет два важных целей, различающихся по состояние флага SOF_UNIQUEFILENAME.</span><span class="sxs-lookup"><span data-stu-id="5bac9-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="5bac9-155">Если этот флаг не задан, **OpenStreamOnFile** открывает объект **IStream** на существующий файл, например скопировать его содержимое вложения с помощью **IStream со значением свойства **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) :: CopyTo** метод.</span><span class="sxs-lookup"><span data-stu-id="5bac9-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="5bac9-156">В этом случае параметр _lpszFileName_ указывает путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="5bac9-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="5bac9-157">Если для SOF_UNIQUEFILENAME, **OpenStreamOnFile** создает временный файл для хранения данных для объекта **IStream** .</span><span class="sxs-lookup"><span data-stu-id="5bac9-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="5bac9-158">Использования этого параметра _lpszFileName_ при необходимости можно указать путь к папке, где он будет создан, а параметр _lpszPrefix_ при необходимости можно указать префикс для имени файла.</span><span class="sxs-lookup"><span data-stu-id="5bac9-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="5bac9-159">По завершении вызывающему приложению клиента или поставщика услуг с объектом **IStream** , его следует освободить путем вызова метода OLE **IStream::Release** .</span><span class="sxs-lookup"><span data-stu-id="5bac9-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="5bac9-160">MAPI с помощью функции, на который указывает _lpAllocateBuffer_ и _lpFreeBuffer_ для большинства выделение и освобождение памяти, в частности для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объекта, таких как [IMAPIProp:: GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="5bac9-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5bac9-161">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5bac9-161">Notes to callers</span></span>

<span data-ttu-id="5bac9-162">Флаг SOF_UNIQUEFILENAME используется для создания временный файл с именем для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="5bac9-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="5bac9-163">Если установлен этот флаг указывает параметр _lpszFileName_ путь для временный файл, а параметр _lpszPrefix_ содержит указанные символы префикс имени файла.</span><span class="sxs-lookup"><span data-stu-id="5bac9-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="5bac9-164">— Это имя созданного файла <prefix>HHHH. TMP, где HHHH — это шестнадцатеричный номер.</span><span class="sxs-lookup"><span data-stu-id="5bac9-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="5bac9-165">Если _lpszFileName_ имеет значение NULL, файл будет создан в каталог временных файлов, который возвращается функцией Windows **GetTempPath**, или в текущем каталоге при назначении не каталог временных файлов.</span><span class="sxs-lookup"><span data-stu-id="5bac9-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="5bac9-166">Если флаг SOF_UNIQUEFILENAME не установлен, учитывается, _lpszPrefix_ и _lpszFileName_ должен содержать полный путь и имя файла, который требуется открыть или создать.</span><span class="sxs-lookup"><span data-stu-id="5bac9-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="5bac9-167">Файл будет открыт или создан на основании других метки, установленные в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="5bac9-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5bac9-168">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="5bac9-168">MFCMAPI reference</span></span>

<span data-ttu-id="5bac9-169">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="5bac9-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5bac9-170">**����**</span><span class="sxs-lookup"><span data-stu-id="5bac9-170">**File**</span></span>|<span data-ttu-id="5bac9-171">**�������**</span><span class="sxs-lookup"><span data-stu-id="5bac9-171">**Function**</span></span>|<span data-ttu-id="5bac9-172">**�����������**</span><span class="sxs-lookup"><span data-stu-id="5bac9-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5bac9-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="5bac9-173">File.cpp</span></span>  <br/> |<span data-ttu-id="5bac9-174">WriteAttachStreamToFile</span><span class="sxs-lookup"><span data-stu-id="5bac9-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="5bac9-175">Mfcmapi (en) использует метод **OpenStreamOnFile** открыты потока в файл записывается вложения на него.</span><span class="sxs-lookup"><span data-stu-id="5bac9-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bac9-176">См. также</span><span class="sxs-lookup"><span data-stu-id="5bac9-176">See also</span></span>



[<span data-ttu-id="5bac9-177">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5bac9-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

