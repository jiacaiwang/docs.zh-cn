---
title: "ISymUnmanagedReader::GetMethodFromDocumentPosition 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedReader.GetMethodFromDocumentPosition
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedReader::GetMethodFromDocumentPosition
helpviewer_keywords:
- GetMethodFromDocumentPosition method [.NET Framework debugging]
- ISymUnmanagedReader::GetMethodFromDocumentPosition method [.NET Framework debugging]
ms.assetid: 55773dbc-9053-46e3-8a3c-86caa9d91fb4
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: ad64d5722df68859e7be9d44b94b95cf1f43823f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedreadergetmethodfromdocumentposition-method"></a><span data-ttu-id="c31b3-102">ISymUnmanagedReader::GetMethodFromDocumentPosition 方法</span><span class="sxs-lookup"><span data-stu-id="c31b3-102">ISymUnmanagedReader::GetMethodFromDocumentPosition Method</span></span>
<span data-ttu-id="c31b3-103">返回包含在文档中的给定位置处的断点的方法。</span><span class="sxs-lookup"><span data-stu-id="c31b3-103">Returns the method that contains the breakpoint at the given position in a document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c31b3-104">语法</span><span class="sxs-lookup"><span data-stu-id="c31b3-104">Syntax</span></span>  
  
```  
HRESULT GetMethodFromDocumentPosition (  
    [in]  ISymUnmanagedDocument*  document,  
    [in]  ULONG32  line,  
    [in]  ULONG32  column,  
    [out, retval] ISymUnmanagedMethod**  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c31b3-105">参数</span><span class="sxs-lookup"><span data-stu-id="c31b3-105">Parameters</span></span>  
 `document`  
 <span data-ttu-id="c31b3-106">[in]指定的文档。</span><span class="sxs-lookup"><span data-stu-id="c31b3-106">[in] The specified document.</span></span>  
  
 `line`  
 <span data-ttu-id="c31b3-107">[in]指定的文档的行。</span><span class="sxs-lookup"><span data-stu-id="c31b3-107">[in] The line of the specified document.</span></span>  
  
 `column`  
 <span data-ttu-id="c31b3-108">[in]指定的文档的列。</span><span class="sxs-lookup"><span data-stu-id="c31b3-108">[in] The column of the specified document.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="c31b3-109">[out]指向的地址的指针[ISymUnmanagedMethod 接口](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)表示包含该断点的方法的对象。</span><span class="sxs-lookup"><span data-stu-id="c31b3-109">[out] A pointer to the address of a [ISymUnmanagedMethod Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) object that represents the method containing the breakpoint.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c31b3-110">返回值</span><span class="sxs-lookup"><span data-stu-id="c31b3-110">Return Value</span></span>  
 <span data-ttu-id="c31b3-111">如果该方法成功; 则为 S_OK否则为 E_FAIL 或某些其他错误代码。</span><span class="sxs-lookup"><span data-stu-id="c31b3-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c31b3-112">要求</span><span class="sxs-lookup"><span data-stu-id="c31b3-112">Requirements</span></span>  
 <span data-ttu-id="c31b3-113">**标头：** CorSym.idl、 CorSym.h</span><span class="sxs-lookup"><span data-stu-id="c31b3-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c31b3-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c31b3-114">See Also</span></span>  
 [<span data-ttu-id="c31b3-115">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="c31b3-115">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)