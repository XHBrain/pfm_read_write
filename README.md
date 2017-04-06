# pfm_read_write
test code:
MATLAB:
  P = './';
  D = dir([P '*.pfm']);
  for i = 1 : length(D)
      [img, scaleFactor] = parsePfm([P D(i).name]);
      figure;imshow(img);
      imin = min(img(:));
      imax = max(img(:));
      iimg = (img-imin) / (imax-imin);
      figure;imshow(iimg);
  end

PYTHON
# python convert_pfm_numpy
