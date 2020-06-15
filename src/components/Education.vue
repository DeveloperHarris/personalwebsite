<template>
  <div class="education">
    <div class="edu_core_info">
      <div class="school_crest">
        <img id="byu_logo" src="../assets/byu.png" />
      </div>
      <div class="school_info">
        <div class="top_info">
          <div class="degree">Bachelor of Science in Computer Science</div>
          <div class="school_full_name">Brigham Young University</div>
        </div>
        <div class="additional_info">
          <div class="grad_info">
            <div class="grad_year_header">Expected Graduation:&nbsp;</div>
            <div class="grad_year">December 2021</div>
          </div>
          <div class="gpa">
            <div class="gpa_header">GPA:&nbsp;</div>
            <div class="gpa_num">3.1</div>
          </div>
        </div>
      </div>
    </div>
    <div class="coursework">
      <div class="coursework_header">Relevant Coursework:</div>
      <div class="courses">
        Data Structures & Algorithms
        <br />Algorithm Design & Analysis <br />Web Programming <br />Discrete
        Structures <br />Intro to Computer Systems <br />Advanced Programming
        Concepts <br />Theory of Computation
      </div>
      <div class="condensedCourses">
        Data Structures & Algorithms, Algorithm Design & Analysis, Web
        Programming, Discrete Structures, Intro to Computer Systems, Advanced
        Programming Concepts, Theory of Computation
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Education",
};
</script>

<style>
.education {
  width: 873px;
  height: 177px;
  background: #ffffff;
  box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.25);

  display: flex;
  justify-content: space-between;
}

.edu_core_info {
  display: flex;
  justify-content: start;
}

.school_crest {
  margin: 0 15px;
  height: 100%;
  width: auto;
  display: flex;
  align-items: center;
}

#byu_logo {
  height: 125px;
  width: 125px;
}

.school_info {
  margin: 30px 0;
  text-align: left;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.degree {
  font-weight: 600;
  font-size: 18px;
}

.school_full_name {
  font-weight: 300;
}

.grad_year_header,
.grad_year,
.gpa_num,
.grad_year_header,
.gpa_header {
  display: inline;
  font-size: 14px;
}

.grad_year_header,
.gpa_header {
  font-weight: 600;
}

.gpa_num {
  font-weight: 300;
}

.coursework {
  width: 228px;
  text-align: left;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-right: 15px;
}

.coursework_header,
.courses,
.condensedCourses {
  font-size: 12px;
}
.coursework_header {
  font-weight: 600;
}
.courses {
  font-weight: 300;
}

.condensedCourses {
  display: none;
}

@media screen and (max-width: 1820px) and (min-width: 421px) {
  .education {
    flex-direction: column;
    justify-content: space-evenly;
    height: 100%;
    width: auto;
    padding: 10px;
  }

  .edu_core_info {
    width: 100%;
  }

  .school_info {
    margin: 10px 0;
  }

  #byu_logo {
    height: 100px;
    width: 100px;
  }

  .coursework {
    width: 100%;
    margin-top: 10px;
  }

  .courses {
    display: none;
  }

  .condensedCourses {
    display: block;
    width: 100%;
  }
}

@media screen and (max-width: 1200px) and (min-width: 421px) {
  .edu_core_info {
    flex-direction: column;
  }
}

@media screen and (max-width: 420px) {
  .education {
    width: 100%;
    height: 100%;
    flex-direction: column;
    padding: 10px 0;
  }

  .edu_core_info {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .school_info,
  .coursework {
    text-align: center;
  }

  .coursework {
    width: 100%;
  }
}
</style>
